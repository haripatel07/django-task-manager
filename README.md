# **Task Management System API**

A back-end project designed to help users efficiently create, manage, and track their tasks. This API provides a secure, organized way to handle personal tasks, serving as a robust foundation for a front-end application.

#### **Features**

  * **User Authentication**: Secure user access using JWT (JSON Web Tokens).
  * **Task Management**: Create, read, update, and delete tasks.
  * **Status Tracking**: Organize tasks with categories like Pending, In Progress, and Completed.
  * **Priority Setting**: Set priorities (Low, Medium, High) to focus on important tasks.

-----

#### **Technologies**

  * **Django**: A high-level Python web framework for rapid development.
  * **Django REST Framework**: A powerful toolkit for building RESTful APIs.
  * **PostgreSQL**: A robust relational database system.
  * **Simple JWT**: For secure token-based authentication.
  * **Gunicorn**: A production-grade Python WSGI server.
  * **python-decouple**: For managing environment variables.

-----

### **Getting Started**

These instructions will get you a copy of the project up and running on your local machine for development and testing.

#### **Prerequisites**

Ensure you have Python and PostgreSQL installed.

```bash
python --version
psql --version
```

#### **Installation**

1.  Clone the repository:
    ```bash
    git clone https://github.com/your-username/django-task-manager.git
    cd django-task-manager
    ```
2.  Create and activate a virtual environment:
    ```bash
    python3 -m venv venv
    source venv/bin/activate
    ```
3.  Install the required packages:
    ```bash
    pip install -r requirements.txt
    ```
4.  Set up your PostgreSQL database and create a `.env` file in the project's root with your credentials:
    ```
    SECRET_KEY=your_very_long_and_random_secret_key_here
    DEBUG=True
    DATABASE_NAME=task_manager_db
    DATABASE_USER=your_username
    DATABASE_PASSWORD=your_password
    DATABASE_HOST=localhost
    DATABASE_PORT=5432
    ```
5.  Run database migrations:
    ```bash
    python manage.py makemigrations tasks
    python manage.py migrate
    ```
6.  Create a superuser to access the API:
    ```bash
    python manage.py createsuperuser
    ```
7.  Start the development server:
    ```bash
    python manage.py runserver
    ```
    Your API will be accessible at `http://127.0.0.1:8000/`.

-----

### **Deployment**

This back end is deployed on Render's platform.

  * **Live URL**: `https://django-task-manager-2ukd.onrender.com`

-----

### **API Endpoints**

All API endpoints are prefixed with `/api/`. Test them using a tool like Postman.

#### **1. User Authentication**

  * **`POST /api/register/`**: Create a new user account.
  * **`POST /api/token/`**: Obtain a JWT access token using user credentials.

#### **2. Task Management**

  * **`GET /api/tasks/`**: Retrieve all tasks for the authenticated user.
  * **`POST /api/tasks/`**: Create a new task.
  * **`GET /api/tasks/<id>/`**: Retrieve a specific task.
  * **`PATCH /api/tasks/<id>/`**: Update a task.
  * **`DELETE /api/tasks/<id>/`**: Delete a task.

-----

### **License**

This project is licensed under the **MIT License**.
