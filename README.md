#  BLCKey Core

**BlcKEY Core** is the foundational component of the innovative Web3 authentication platform **[BlcKEY.com](https://blckey.com)**, based on the **Taler (TLR)** blockchain. The platform enables secure, anonymous authentication to Web3 services without passwords, emails, or KYC—using only QR codes and cryptographic signatures.

---
Purpose of publication

- To fix the authorship of the idea and architecture
- Protect against third-party patenting attempts
- Define licence boundaries and right holder
---

## Key Features

- Authentication via QR codes and cryptographic signatures  
- Secure local storage of keys and seed phrases  
- Stateless authentication without usernames, passwords, or KYC  
- Support for multiple independent Web3 services on a single device (via BIP-44 accounts)  
- WebSocket sessions and real-time sync of authentication status  

---

## Documentation

Full documentation is available in the [docs/](docs/README.md) folder:

### Core Documents
- [README](docs/README.md) – Overview of documentation structure  
- [USE CASES](docs/USECASE.md) – Common usage scenarios and flows  
- [UI FLOW](docs/UI_FLOW.md) – Screens, transitions, user interactions  

### Developer Documentation
- [API Reference](docs/API.md) – Endpoints and parameters  
- [SDK Integration Guide](docs/SDK.md) – Integrate BlcKEY with your app  
- [Cryptography Overview](docs/CRYPTOGRAPHY.md) – Algorithms and key generation  
- [Testing Guidelines](docs/TESTING.md) – Testing procedures and tools  

### Security
- [Security & Data Protection](docs/SECURITY.md) – Threat model and storage policies  

---

## Project Structure

```
BlcKEY-Core-EN/
├── backend/               # FastAPI backend server for authentication
├── client-server/         # Local FastAPI client logic (mobile/desktop agent)
├── flutter-client/        # Flutter app (UI + local storage)
├── examples/              # Sample use cases and test setups
├── docs/                  # All user and developer documentation
│   ├── README.md
│   ├── API.md
│   ├── SDK.md
│   ├── CRYPTOGRAPHY.md
│   ├── UI_FLOW.md
│   ├── SECURITY.md
│   ├── TESTING.md
│   └── USECASE.md
├── licenses/              # Licensing models
│   ├── LICENSE_COMMUNITY.md
│   ├── LICENSE_NON_COMMERCIAL.md
│   └── LICENSE_COMMERCIAL.md
├── README.md              # Project overview (you are here)
└── LICENSE.md             # Summary of license conditions
```

---

## Licensing

BlcKEY Core uses a **multi-tier licensing model** to support open-source use, non-commercial research, and enterprise integration:

### [Community License](licenses/LICENSE_COMMUNITY.md)
- Free for personal, educational, and research use  
- Commercial use is strictly prohibited without agreement  

### [Non-Commercial License](licenses/LICENSE_NON_COMMERCIAL.md)
- Access to closed components under limited non-commercial terms  
- Requires approval from the BlcKEY Core team  

### [Commercial License](licenses/LICENSE_COMMERCIAL.md)
- Grants full integration and usage rights  
- Allows commercial deployment with SLA-backed support  
- Prohibits blockchain adaptation or patent claims without written consent  

> **Blockchain Restriction**:  
> This technology is licensed for exclusive use with the **Taler (TLR)** blockchain.  
> Any adaptation to other chains or crypto systems requires explicit written permission from the BlcKEY Core team.

---

##  Contact

For licensing inquiries, support contracts, or commercial partnerships:  
**contact [at] blckey [dot] com**  
**[https://blckey.com](https://blckey.com)**

# HASH: 70048e460c4ad3036920ea5396ba8efc2a07bd5e40df48f00af09e62f2a29e29
# ADDRESS: TN9NBaq1YXEM3posuQqL5j3pCwBZoKh97K
# SIGNATURE: 26f0269425d396006597cfe87aa34bc4556442c131b4b43bbb6f1deb3c53c8101e55007439a0f2a3c481cc790e245099e800ff549441b1330f2255dba5825c71
