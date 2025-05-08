# Mini Blog API

A Django REST Framework API for a mini blog with comments functionality.

## Features

- User authentication with JWT
- CRUD operations for blog posts
- Comment system for posts
- Permission-based access control
- Post filtering and search

## Setup

1. Create a virtual environment:
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

2. Install dependencies:
```bash
pip install -r requirements.txt
```

3. Run migrations:
```bash
python manage.py migrate
```

4. Create a superuser:
```bash
python manage.py createsuperuser
```

5. Run the development server:
```bash
python manage.py runserver
```

## API Endpoints

- `GET /api/posts/` - List all posts
- `POST /api/posts/` - Create a new post
- `GET /api/posts/<id>/` - Get post details
- `PUT/PATCH /api/posts/<id>/` - Update a post
- `DELETE /api/posts/<id>/` - Delete a post
- `POST /api/posts/<id>/comments/` - Add a comment to a post
- `GET /api/posts/<id>/comments/` - Get comments for a post

## Authentication

The API uses JWT authentication. To get a token:

1. Register: `POST /api/auth/register/`
2. Login: `POST /api/auth/token/`

Use the token in the Authorization header: `Bearer <token>` 