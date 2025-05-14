# BlcKEY Core API Documentation

## Base URL
```
https://your-blckey-service.com/api/v1
```

---

## API Methods and Request Examples

### 1. Get QR Code for Client Registration

**GET** `/auth/qr`

**Response:**
```json
{
  "challenge": "<server-generated challenge>",
  "server_pubkey": "<server public key>",
  "server_account": 0,
  "service_domain": "blckey.com",
  "qr_code_url": "<QR code URL>"
}
```

---

### 2. Register Client

**POST** `/auth/register`

**Request (JSON):**
```json
{
  "client_pubkey": "<client public key>",
  "client_address": "<client address>",
  "challenge": "<server challenge>",
  "signed_challenge": "<client-signed challenge>"
}
```

**Response:**
```json
{
  "status": "registered",
  "client_pubkey": "<client public key>"
}
```

**Errors:**
- `400` � Challenge not found / invalid signature / address mismatch.

---

### 3. Request Login Challenge

**POST** `/auth/request-login-challenge`

**Request (JSON):**
```json
{
  "client_pubkey": "<client public key>",
  "signed_challenge": "<signed 'request_challenge' string>"
}
```

**Response:**
```json
{
  "login_challenge": "<login challenge>",
  "signed_by_server": "<challenge signed by server>",
  "server_pubkey": "<server public key>"
}
```

**Errors:**
- `403` � Client not registered / invalid request signature.

---

### 4. Confirm Login (Authentication)

**POST** `/auth/confirm-login`

**Request (JSON):**
```json
{
  "client_pubkey": "<client public key>",
  "signed_challenge": "<client-signed login challenge>"
}
```

**Response:**
```json
{
  "status": "logged_in"
}
```

**Errors:**
- `403` � Challenge not found / invalid signature.

---

### 5. Logout

**POST** `/auth/logout`

**Request (JSON):**
```json
{
  "client_pubkey": "<client public key>",
  "signed_challenge": "<signed 'logout_request' string>"
}
```

**Response:**
```json
{
  "status": "logged_out"
}
```

**Errors:**
- `403` � Invalid logout signature.

---

## Common Error Response Format

```json
{
  "detail": "Error description"
}
```

---

## Interaction Logic

### Registration:
- Client receives a QR code with a challenge.
- Signs the challenge with a private key and sends the public key and address to the server.
- Server verifies and registers the client.

### Authentication:
- Client requests a login challenge by sending a signed 'request_challenge'.
- Server returns a login challenge signed by itself.
- Client signs and returns this challenge.
- Server verifies the signature and creates a session.

### Logout:
- Client sends a logout request signed as 'logout_request'.
- Server immediately terminates the session.

# HASH: 04bd462ad925debbdc97309e0ab5b2fdccc1a02b87fc181a50f076c9a99a0762
# ADDRESS: TN9NBaq1YXEM3posuQqL5j3pCwBZoKh97K
# SIGNATURE: 7b5ae0231981baaab760d9744330dd5cedd28460e50eeeeeda338911c5368339b53e3eb25c268c7061c129b3bffcea860f51af01dfc3abe6868d5165f0c04719
