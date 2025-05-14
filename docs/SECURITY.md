# BlcKEY Core Security & Data Protection

BlcKEY Core adheres to stringent security standards and best practices to ensure the highest level of privacy, anonymity, and trust minimization.

---

## Data Protection Principles

### Seed Phrase Security

- **Seed phrases never leave user devices.**
- Generated and stored locally in secure storage.
- No remote transmission or storage of seed phrases.

### Private Key Storage

- **Private keys stored only locally.**
- Never transmitted to servers or exposed via API endpoints.

### Data Minimization

- Only public keys, addresses, and cryptographic signatures are transmitted to servers.

---

## Sensitive Information Storage

### Local Storage (Flutter Client)

- Seed phrases and private keys are securely stored using device-specific secure storage:
  - Keychain on iOS.
  - KeyStore on Android.
  - Encrypted storage on desktop devices.

### Server-side Storage

- Temporary data (e.g., cryptographic challenges, session states) stored in Redis with short expiration (TTL).
- Servers never store users' private keys or seed phrases.

---

## Authentication and Session Management

### Stateless Authentication

- Authentication conducted through cryptographic signing of temporary challenges.
- No persistent credentials (usernames/passwords) required.

### Session Handling

- Short-lived session tokens managed via cryptographic signatures and temporary storage.
- Sessions terminate upon explicit logout actions or after a defined TTL.

---

## Mutual Authentication

- Client and server authenticate each other through exchange and verification of cryptographic challenges and signatures, preventing man-in-the-middle (MITM) attacks.

---

## Transport Layer Security (TLS/HTTPS)

- All communication between client and server secured by HTTPS protocol (TLS).

---

## Recommended User Practices

- **Keep seed phrases secure:** Never share them with third parties.
- **Use trustworthy devices:** Ensure your device is free of malware.
- **Regularly update software:** Always use the latest version of BlcKEY Core.

---

## Monitoring and Logging

- Operation logs maintained for registration and authentication.
- Logs exclude private keys, seed phrases, and other sensitive data.
- Regular security audits conducted to maintain integrity.

# HASH: 286359a57b1e9090ddf98b2377cabd4ce6a335e9b035b2269d531f90b36e9304
# ADDRESS: TN9NBaq1YXEM3posuQqL5j3pCwBZoKh97K
# SIGNATURE: d059522ddaf22e6b8051ba7bdf317212304d98b804775e4d9fe3d85f2da275e9086636820b2b9f2ac9f87db092997d71af10f478083cec20942e51df139dcdc3
