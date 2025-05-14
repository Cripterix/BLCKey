# BlcKEY Core Use Case Scenario

## User Registration Flow:
1. User visits a Web3 service website and initiates registration.
2. The website generates and displays a QR code containing a unique cryptographic challenge and server public key.
3. User scans this QR code with the BlcKEY mobile app.
4. The app generates a client-side cryptographic key pair specific to this service.
5. User signs the received challenge using the generated private key.
6. The signed challenge along with the user's public key and generated address is sent to the service backend.
7. The backend verifies the signature, stores the user’s public key, and confirms the registration.

## User Authentication (Login/Logout) Flow:
1. User selects the registered service in the BlcKEY app.
2. To log in, the User slides the authentication slider to "Log In."
3. The app sends a signed login-challenge request to the service backend.
4. The backend responds with a new cryptographic challenge signed by its server private key.
5. User verifies the server signature and signs this new challenge.
6. The signed challenge is sent back to the backend, which validates the signature and authenticates the user.
7. Upon successful verification, the user is logged in.

## Logout:
- User slides the authentication slider to "Log Out."
- The app sends a signed logout request.
- The backend verifies and logs the user out securely.

# HASH: bf5025480004d87a9e2af2d063e30cd79a04b34f6dcc5104c29d775298f28066
# ADDRESS: TN9NBaq1YXEM3posuQqL5j3pCwBZoKh97K
# SIGNATURE: 5ce2ba6a3d283a82cc67eadafb1fcf3e6d7255e51bd2ee90baa9cab8160ca71e93c80630985cc0abfb75e4ac828b460d364ea1d3f60ad69fba122266424b6cf2
