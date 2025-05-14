# BlcKEY Core SDK Integration Guide

The BlcKEY Core SDK simplifies the integration of secure, passwordless Web3 authentication using QR codes and cryptographic signatures based on the Taler (TLR) blockchain.

---

## SDK Features:

- Request user registration via QR code.
- Confirm registration with cryptographic signatures.
- Authenticate users (login/logout) through cryptographic challenges.
- Stateless authentication without storing passwords or usernames.

---

## Integration Steps

### Step 1: User Registration

**1. Obtain a registration QR code:**
```http
GET /auth/qr
```

**2. Sign the challenge and send data:**
```http
POST /auth/register
```

**Python request example:**
```python
requests.post(url + "/auth/register", json={
    "client_pubkey": client_pubkey,
    "client_address": client_address,
    "challenge": challenge,
    "signed_challenge": signed_challenge
})
```

---

### Step 2: User Authentication

**1. Request login challenge:**
```http
POST /auth/request-login-challenge
```

**2. Sign challenge and send back to server:**
```http
POST /auth/confirm-login
```

**Python request example:**
```python
requests.post(url + "/auth/request-login-challenge", json={
    "client_pubkey": client_pubkey,
    "signed_challenge": signed_request_challenge
})

requests.post(url + "/auth/confirm-login", json={
    "client_pubkey": client_pubkey,
    "signed_challenge": signed_login_challenge
})
```

---

### Step 3: User Logout

Request logout:
```http
POST /auth/logout
```

**Python request example:**
```python
requests.post(url + "/auth/logout", json={
    "client_pubkey": client_pubkey,
    "signed_challenge": signed_logout_request
})
```

---

## SDK Class & Methods (Pseudo-code)

**Example Python SDK class:**
```python
class BlcKeyAuthClient:
    def __init__(self, base_url: str, client_pubkey: str, client_address: str):
        self.base_url = base_url
        self.client_pubkey = client_pubkey
        self.client_address = client_address

    def get_registration_qr(self):
        pass  # get registration QR with challenge

    def register(self, signed_challenge: str):
        pass  # send registration data

    def request_login_challenge(self, signed_request: str):
        pass  # request login challenge

    def confirm_login(self, signed_challenge: str):
        pass  # confirm authentication

    def logout(self, signed_logout_request: str):
        pass  # logout
```

---

## SDK Usage Example

**Python Integration:**
```python
from blckey_sdk import BlcKeyAuthClient

client = BlcKeyAuthClient(base_url="https://your-blckey-service.com/api/v1",
                          client_pubkey="your_pubkey",
                          client_address="your_address")

# Registration
qr_info = client.get_registration_qr()
signed_challenge = your_sign_method(qr_info['challenge'])
client.register(signed_challenge)

# Authentication
login_challenge = client.request_login_challenge(your_sign_method('request_challenge'))
client.confirm_login(your_sign_method(login_challenge))

# Logout
client.logout(your_sign_method('logout_request'))
```

---

## Integration Requirements:

- Support for HTTP/HTTPS requests (HTTPS recommended).
- Ability to perform ECDSA SECP256k1 cryptographic signing.
- JSON format required for all interactions.

# HASH: 0a293a677271a650a5d069c24a188c2e260bad8113619f900f966ed5e5fe7580
# ADDRESS: TN9NBaq1YXEM3posuQqL5j3pCwBZoKh97K
# SIGNATURE: 83fd72b0fb771c656a13540b101eedd3692339ea6b4fa88ca3450a86203221f1d0fcd391ba9b0cbf9343783e230bb6b74d52c35d54aa4f8a6659ed871a0bbc35
