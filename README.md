# URL Shortener API

A FastAPI-based URL Shortener service.

## Setup Instructions

### 1. Create & activate virtual environment
```bash
python -m venv venv

# Windows
venv\Scripts\activate

# Mac/Linux
source venv/bin/activate
```

### 2. Install dependencies
```bash
pip install -r requirements.txt
```

### 3. Run the server
```bash
uvicorn main:app --reload
```

### 4. Open Swagger UI to test
```
http://127.0.0.1:8000/docs
```

## API Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| POST | `/shorten` | Submit a long URL, get a short code |
| GET | `/{short_code}` | Redirects to the original URL |
| GET | `/stats/{short_code}` | Returns original URL + access count |
