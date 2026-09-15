# IndustryHub - Industrial Approvals & Compliance Platform

A dual-sided platform streamlining industrial approvals, compliance processes, and access to government support services.

## Project Structure

```
industryhub/
├── backend/          # Django REST API
├── frontend/         # React application
├── docs/             # Documentation
```

## Tech Stack

**Backend:**
- Django 4.2
- Django REST Framework
- PostgreSQL
- JWT Authentication

**Frontend:**
- React 18
- Material-UI
- Axios
- React Router

## Setup Instructions

### Prerequisites

- Python 3.10+
- Node.js 18+
- PostgreSQL 14+

### Backend Setup

1. Navigate to backend directory:
   ```bash
   cd backend
   ```

2. Create and activate virtual environment:
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

4. Create `.env` file (copy from `.env.example`):
   ```bash
   cp .env.example .env
   ```

5. Update `.env` with your database credentials

6. Run migrations:
   ```bash
   python manage.py migrate
   ```

7. Create superuser:
   ```bash
   python manage.py createsuperuser
   ```

8. Run development server:
   ```bash
   python manage.py runserver
   ```

Backend API will be available at http://localhost:8000

### Frontend Setup

1. Navigate to frontend directory:
   ```bash
   cd frontend
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Create `.env` file:
   ```bash
   echo "REACT_APP_API_URL=http://localhost:8000/api" > .env
   ```

4. Start development server:
   ```bash
   npm start
   ```

Frontend will be available at http://localhost:3000

## API Endpoints

### Authentication
- `POST /api/users/register/` - Register new user
- `POST /api/users/login/` - Login (returns JWT tokens)
- `POST /api/users/token/refresh/` - Refresh access token
- `GET /api/users/profile/` - Get current user profile

## Development

### Running Tests

**Backend:**
```bash
cd backend
python manage.py test
```

**Frontend:**
```bash
cd frontend
npm test
```

### Database Migrations

When models change:
```bash
python manage.py makemigrations
python manage.py migrate
```

## Team

- Backend Team: Django API development
- Frontend Team: React UI development
- Full Stack: Integration and testing

## License

MIT License
