# School Portal System

A full-stack school portal system built with Django and React. The project is intended to provide a central platform for managing school users, academic records, communication, and administrative workflows.

## Technology Stack

- **Backend:** Django
- **Frontend:** React
- **Database:** Configurable through Django settings
- **API:** Django-based REST API
- **Package Management:** `pip` for backend dependencies and `npm` or `yarn` for frontend dependencies

## Features

The system can be extended to support:

- Student, teacher, parent, and administrator accounts
- Student profile and enrollment management
- Class, subject, and academic session management
- Attendance tracking
- Result and grade management
- Announcements and school communication
- Role-based access control
- Dashboard views for different user types

## Project Structure

A typical structure for this project may look like this:

```text
school-portal-system/
├── backend/          # Django project and apps
├── frontend/         # React application
├── README.md
└── .git/
```

If your folders use different names, update this section after the backend and frontend have been added.

## Getting Started

### Prerequisites

Make sure you have the following installed:

- Python 3.10 or later
- Node.js 18 or later
- npm or yarn
- Git

## Backend Setup

From the project root:

```bash
cd backend
python -m venv venv
source venv/bin/activate
pip install -r requirements.txt
python manage.py migrate
python manage.py createsuperuser
python manage.py runserver
```

The Django backend should be available at:

```text
http://127.0.0.1:8000/
```

## Frontend Setup

From the project root:

```bash
cd frontend
npm install
npm run dev
```

Depending on the React setup, the frontend may be available at:

```text
http://localhost:5173/
```

For Create React App projects, use:

```bash
npm start
```

and visit:

```text
http://localhost:3000/
```

## Environment Variables

Create environment files as needed for local development.

Example backend variables:

```env
SECRET_KEY=your-django-secret-key
DEBUG=True
ALLOWED_HOSTS=127.0.0.1,localhost
DATABASE_URL=your-database-url
```

Example frontend variables:

```env
VITE_API_BASE_URL=http://127.0.0.1:8000/api
```

Use `REACT_APP_API_BASE_URL` instead if the frontend is created with Create React App.

## Common Commands

### Django

```bash
python manage.py runserver
python manage.py makemigrations
python manage.py migrate
python manage.py createsuperuser
python manage.py test
```

### React

```bash
npm run dev
npm run build
npm test
```

## API Overview

The backend should expose API endpoints for the frontend to consume. Common endpoint groups may include:

- `/api/auth/`
- `/api/students/`
- `/api/teachers/`
- `/api/classes/`
- `/api/subjects/`
- `/api/attendance/`
- `/api/results/`
- `/api/announcements/`

Update this section with the exact endpoints once the backend API is implemented.

## Development Workflow

1. Start the Django backend server.
2. Start the React frontend development server.
3. Configure the frontend API base URL to point to the backend.
4. Build features in small, testable sections.
5. Run backend and frontend tests before pushing changes.

## Deployment Notes

Before deploying:

- Set `DEBUG=False`
- Configure production `ALLOWED_HOSTS`
- Use a secure `SECRET_KEY`
- Configure a production database
- Collect Django static files if needed
- Build the React frontend for production
- Configure CORS and CSRF settings correctly

## Contributing

1. Clone the repository.
2. Create a new branch for your feature or fix.
3. Make your changes.
4. Run tests.
5. Submit a pull request.

## License

This project does not currently specify a license. Add one before distributing or deploying it publicly.
