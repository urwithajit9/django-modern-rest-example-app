# Test app for Django Modern REST - django_test_app

## Reference

Original project: https://github.com/wemake-services/django-modern-rest

Documentation and Read more: https://django-modern-rest.readthedocs.io/en/latest/


## Project Structure

```

django_test_app
├── README.md
├── manage.py
├── mypy.ini
└── server
├── __init__.py
├── apps
│   ├── __init__.py
│   ├── controllers
│   │   ├── __init__.py
│   │   ├── auth.py
│   │   ├── urls.py
│   │   └── views.py
│   ├── django_session_auth
│   │   ├── __init__.py
│   │   ├── urls.py
│   │   └── views.py
│   ├── jwt_auth
│   │   ├── __init__.py
│   │   ├── urls.py
│   │   └── views.py
│   ├── middlewares
│   │   ├── __init__.py
│   │   ├── middleware.py
│   │   ├── urls.py
│   │   └── views.py
│   ├── models_example
│   │   ├── __init__.py
│   │   ├── migrations
│   │   │   ├── 0001_initial.py
│   │   │   └── __init__.py
│   │   ├── models.py
│   │   ├── serializers.py
│   │   ├── services.py
│   │   ├── urls.py
│   │   └── views.py
│   ├── negotiations
│   │   ├── __init__.py
│   │   ├── urls.py
│   │   └── views.py
│   └── openapi
│       ├── __init__.py
│       └── config.py
├── asgi.py
├── settings.py
├── urls.py
└── wsgi.py

```

## Overview

- **`manage.py`** – Django CLI entry point  
- **`server/`** – Core Django project
  - **`apps/`** – Modular application components
    - `controllers/` – Core request handling logic
    - `django_session_auth/` – Session-based authentication
    - `jwt_auth/` – JWT-based authentication
    - `middlewares/` – Custom middleware logic
    - `models_example/` – Example models with services & serializers
    - `negotiations/` – Business logic module
    - `openapi/` – API schema/config
  - **`settings.py`** – Project configuration
  - **`urls.py`** – Root URL routing
  - **`asgi.py` / `wsgi.py`** – Deployment entry points

## Notes

- Structured for **modular Django app architecture**
- Separates:
  - **auth strategies (JWT vs session)**
  - **business logic (`services.py`)**
  - **API layer (`views.py`, `serializers.py`)**
- Includes **type checking (`mypy.ini`)**


