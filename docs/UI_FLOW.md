# BlcKEY Core UI Flow and User Scenarios

BlcKEY Core provides a streamlined, intuitive interface enabling users to securely authenticate with Web3 services through QR codes and cryptographic signatures.

---

## Main Screens and Scenarios

### 1. Seed Phrase Setup (SeedSetupScreen)

**Purpose:** Create a new or restore an existing seed phrase.

**User Actions:**
- Generate a new seed phrase or input an existing one.
- Seed phrase is stored securely in local storage.

---

### 2. Services List Screen (ServicesListScreen)

**Purpose:** View all connected services and their current authentication status.

**Functionality:**
- Display service list.
- Show authentication status (Logged in / Logged out).
- Navigate to service details (ServiceCardScreen).
- Add new services via QR registration.

---

### 3. Service Card Screen (ServiceCardScreen)

**Purpose:** Display service details and manage login/logout.

**Functionality:**
- Display service domain and public key.
- Slider for login/logout actions.
- Real-time authentication status updates.

**Authentication Slider Workflow:**
- User slides right to log in.
- Slider changes color upon successful authentication.
- User slides left to log out.

---

### 4. QR Service Registration (QrRegisterScreen)

**Purpose:** Register new services by scanning QR codes.

**User Actions:**
- Scan QR code from the service using device camera.
- Receive server challenge.
- Sign challenge and submit data to server.
- On successful registration, service is added to the list.

---

### 5. Service Edit Screen (ServiceEditScreen)

**Purpose:** Manage service parameters (edit or delete).

**Functionality:**
- Display service connection details.
- Option to remove the service from the list.

---

## User Interaction Flow (Scenarios)

### New Service Registration:
```
Seed phrase → Services list → Add service → Scan QR code → Confirm → Registration complete → Service listed
```

### Service Login:
```
Services list → Select service → Slide right (Log In) → Authenticate → Update status (Logged In)
```

### Service Logout:
```
Services list → Select service → Slide left (Log Out) → Session termination → Update status (Logged Out)
```

---

## UX Principles:

- Simple and minimalist interface.
- Clear instructions on each screen.
- Visual feedback upon successful actions.
- Data security (local storage of sensitive information).

# HASH: f34700df27de80c7e5d3775d26fb46ea8ed5fbd2f7244739bb1af82a1234ee5e
# ADDRESS: TN9NBaq1YXEM3posuQqL5j3pCwBZoKh97K
# SIGNATURE: c39ee698d50605cfd24fe21d6f1ba697760064f0c6be0a550aec5b11a5d28145d3a213908512b6172304844e3b496b0c68fb3aaeee0da46de831c7f71ae95cfa
