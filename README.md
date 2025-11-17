This repository contains a small Flask app with two endpoints and a test suite.

**Endpoints**
- **GET /hello**: returns JSON `{"message": "Hello, World!"}` with HTTP status `200`.
- **POST /echo**: accepts a JSON payload and echoes it back with HTTP status `201`.

**Tests**
- **File**: `test_app.py` - contains `test_hello` and `test_echo` using Flask's `test_client()`.
- **Run locally**: `pytest --cov=app test_app.py` (ensure dependencies from `requirements.txt` are installed).

**CI**
- Linting workflow: `.github/workflows/lint.yml` runs `flake8` on `app.py` and `test_app.py`.
- Test workflow: `.github/workflows/test.yml` runs `pytest` across Python 3.10–3.12 and uploads coverage to Codecov (requires `CODECOV_TOKEN` secret to upload successfully).