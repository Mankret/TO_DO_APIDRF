# To-Do List API (Django + DRF)

Simple REST API for managing a list of tasks (To-Do items). The project is built with **Django** and **Django REST Framework**.

---

## 🚀 Features

* Create a task
* Get list of tasks
* Get a single task
* Update task
* Delete task
* Admin panel for managing tasks

---

## 🛠 Tech Stack

* Python 3
* Django
* Django REST Framework
* SQLite (default)
* python-dotenv (environment variables management)

---

## 📦 Project Structure

```
TO_DO_APIDRF/
├── config/            # Project settings and main URLs
├── todos/             # Main application (tasks logic)
│   ├── models.py      # Database models
│   ├── serializers.py # DRF serializers
│   ├── views.py       # API views (ViewSets)
│   ├── urls.py        # API routes
│   └── admin.py       # Admin configuration
├── manage.py
├── requirements.txt
└── .venv/
```

---

## 🔐 Environment Variables

This project uses **python-dotenv** to keep sensitive data (like `SECRET_KEY`) out of the source code.

Create a `.env` file in the project root:

```env
SECRET_KEY=your-secret-key-here
```

Make sure `.env` is added to `.gitignore`.

---

## ⚙️ Setup & Run

### 1. Clone the repository

```bash
git clone https://github.com/Mankret/TO_DO_APIDRF.git
cd TO_DO_APIDRF
```

### 2. Create and activate virtual environment

```bash
python3 -m venv .venv
source .venv/bin/activate
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

### 4. Apply migrations

```bash
python manage.py migrate
```

### 5. Create superuser (optional)

```bash
python manage.py createsuperuser
```

### 6. Run the server

```bash
python manage.py runserver
```

---

## 🌐 API Endpoints

Base URL:

```
http://127.0.0.1:8000/api/
```

| Method | Endpoint     | Description     |
| ------ | ------------ | --------------- |
| GET    | /todos/      | Get all tasks   |
| POST   | /todos/      | Create new task |
| GET    | /todos/{id}/ | Get task by ID  |
| PATCH  | /todos/{id}/ | Update task     |
| DELETE | /todos/{id}/ | Delete task     |

---

## 📝 Example Request

Create a new task:

```http
POST /api/todos/
```

```json
{
  "title": "Learn Django REST Framework"
}
```

---

## 🔐 Admin Panel

```
http://127.0.0.1:8000/admin/
```

Use the superuser credentials to manage tasks via Django Admin.

---

## 📈 Future Improvements

* User authentication (JWT) ✅
* Permissions ✅
* Filtering and search ✅
* Pagination ✅
* Docker support

---

## 👤 Author

Pet project by Mankret for backend development with Django REST Framework.
