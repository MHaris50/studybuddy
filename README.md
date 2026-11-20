# 📚 StudyBudd

A full-stack **study room web application** built with Django, where students can create and join virtual study rooms, chat in real time, filter topics, and manage their profiles.

---

## 🖥️ Features

- 🔐 **Custom Authentication** — Register & log in with email-based authentication
- 🏠 **Study Rooms** — Create, update, and delete topic-based study rooms
- 💬 **Room Chat** — Send messages inside rooms and track participants
- 🔍 **Search & Filter** — Search rooms by topic, name, or description
- 👤 **User Profiles** — View and edit your profile with avatar support
- 📋 **Topics Page** — Browse all available topics
- 📡 **REST API** — Exposes room data via Django REST Framework
- 🌐 **CORS Ready** — Cross-origin support via `django-cors-headers`

---

## 🛠️ Tech Stack

| Layer       | Technology                    |
|-------------|-------------------------------|
| Backend     | Django 6.0.1                  |
| Database    | SQLite3                       |
| Auth        | Custom `AbstractUser` model   |
| API         | Django REST Framework 3.17.1  |
| Images      | Pillow 12.2.0                 |
| CORS        | django-cors-headers 4.9.0     |
| Frontend    | HTML, CSS (Vanilla)           |

---

## 📁 Project Structure

```
studybudd/
├── base/                   # Main Django app
│   ├── api/                # REST API (serializers, views, urls)
│   ├── migrations/         # Database migrations
│   ├── templates/base/     # HTML templates
│   ├── models.py           # User, Room, Topic, Message models
│   ├── views.py            # All view logic
│   ├── forms.py            # Registration, Room, User forms
│   └── urls.py             # App-level URL routing
├── studybudd/              # Project settings & root URLs
├── static/                 # Static assets (CSS, images)
├── templates/              # Global base templates
├── manage.py
└── requirements.txt
```

---

## ⚙️ Setup & Installation

### 1. Clone the repository

```bash
git clone https://github.com/YOUR_USERNAME/studybudd.git
cd studybudd
```

### 2. Create and activate a virtual environment

```bash
# Windows
python -m venv env
env\Scripts\activate

# macOS / Linux
python -m venv env
source env/bin/activate
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

### 4. Apply migrations

```bash
python manage.py migrate
```

### 5. Create a superuser *(optional — for admin access)*

```bash
python manage.py createsuperuser
```

### 6. Run the development server

```bash
python manage.py runserver
```

Visit: [http://127.0.0.1:8000](http://127.0.0.1:8000)

---

## 🔑 Environment Notes

> **Important:** The `db.sqlite3` database file is **not included** in this repository (it is listed in `.gitignore`).  
> After cloning, run `python manage.py migrate` to create a fresh database.

---

## 📡 API Endpoints

| Method | Endpoint  | Description    |
|--------|-----------|----------------|
| GET    | `/api/`   | List all rooms |

The API is built with Django REST Framework and CORS is enabled for all origins in development.

---

## 📸 Pages Overview

| Page           | URL              |
|----------------|------------------|
| Home / Rooms   | `/`              |
| Login          | `/login/`        |
| Register       | `/register/`     |
| Room Detail    | `/room/<id>/`    |
| User Profile   | `/profile/<id>/` |
| Update Profile | `/update-user/`  |
| Topics         | `/topics/`       |
| Activity Feed  | `/activity/`     |

---

## 🧾 .gitignore Recommendations

Make sure your `.gitignore` includes:

```
db.sqlite3
*.pyc
__pycache__/
env/
haris_env/
*.env
static/images/
```

---

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

---

## 🙋‍♂️ Author

**M. Haris**  
Built as a learning project to explore Django full-stack development.
