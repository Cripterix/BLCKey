# BlcKEY Core Testing Guidelines

BlcKEY Core employs automated testing to ensure robust security, reliability, and consistent performance across all system components.

---

## Types of Tests

### 1. Unit Tests
- Test individual functions and methods (cryptographic functions, validation routines, utility functions).
- Implemented using Pytest (Python).

**Running Unit Tests:**
```bash
cd backend
pytest tests/
```

---

### 2. Integration Tests
- Test complete API routes (client requests to server responses), including database interactions (Redis).
- Cover scenarios such as user registration, authentication, and logout.

**Running Integration Tests:**
```bash
cd backend
pytest tests/test_routes_register.py
pytest tests/test_routes_login_challenge.py
pytest tests/test_routes_logout.py
```

---

### 3. Flutter Widget Tests (UI Testing)
- Ensure UI components display correctly and handle user interactions as intended.

**Running Flutter Widget Tests:**
```bash
cd flutter-client
flutter test test/
```

---

## Test Directory Structure

### Backend Server
```
backend/tests/
├── conftest.py
├── pytest.ini
├── test_key_utils.py          # Unit tests for key utilities
├── test_qr_utils.py           # Unit tests for QR code generation/validation
├── test_routes_register.py    # Integration tests for user registration
├── test_routes_login_challenge.py  # Integration tests for login challenge
├── test_routes_logout.py      # Integration tests for logout
├── test_ws_login.py           # WebSocket integration tests
```

### Client-Server (Local)
```
client-server/tests/
├── conftest.py
├── pytest.ini
├── test_key_utils.py
├── test_qr_utils.py
├── test_routes_register.py
├── test_routes_login_challenge.py
├── test_routes_logout.py
├── test_ws_login.py
```

### Flutter Client
```
flutter-client/test/
├── screens_test.dart
├── widgets_test.dart
```

---

## Test Principles

- Tests should be isolated and reproducible.
- Each test should focus on one specific functionality or scenario.
- Utilize assertions to validate expected results and HTTP response statuses.
- Never store private keys or sensitive data within tests.

---

## Recommended Testing Tools

- **Pytest** for backend (Python)
- **Flutter Widget Testing Framework** for client UI

---

## Continuous Integration

- Integrate tests into CI pipelines (GitHub Actions, Jenkins, GitLab CI).
- Automatically run tests on every commit and merge request to ensure continuous code quality.

# HASH: 20ff5b4ae79449aa1558be1a1f1204e3f5c0a8c1603a5585731705b13c285e20
# ADDRESS: TN9NBaq1YXEM3posuQqL5j3pCwBZoKh97K
# SIGNATURE: e9fab71c91911c817bf234cb993351295ac61d0fca811dca1ba74a79ebf1554fc1ffc31955708586ea8450daa50572cb28ef13e4e38dc83fd6621b59039924d8
