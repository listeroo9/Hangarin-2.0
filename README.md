# 📋 Hangarin (Task Management System)

Hangarin is a modern, high-contrast Task Management Dashboard built with **Django**. It helps students and professionals organize their daily goals with subtasks, category filtering, and real-time efficiency tracking.

---

## ✨ Features

* **Social Authentication**: Secure login using **Google** and **GitHub** via `django-allauth`.
* **Dynamic Dashboard**:
    * **Total Tasks**: Tracks your current workload.
    * **Victory Card**: Displays your completion count and a calculated **Efficiency Score**.
    * **Due Soon**: Alerts you to tasks with deadlines within the next 48 hours.
* **Task Management**:
    * **Subtasks**: Break down big goals into smaller, manageable steps.
    * **Notes**: Add sticky-note style details and links to any task.
    * **Priority & Categories**: Organizes tasks with high-contrast, color-coded badges.
* **Search & Filter**: Quickly find tasks by title or filter by specific categories.
* **Modern UI**: High-contrast dark theme with a sticky footer and responsive Bootstrap cards.

---

## 🛠️ Tech Stack

* **Backend**: Django 5.x
* **Frontend**: Bootstrap 5, MDB (Material Design for Bootstrap), FontAwesome Icons
* **Database**: SQLite (Development)
* **Auth**: Django-allauth (OAuth2)
* **Fake Data**: Faker (for database population)

---

## 🚀 Getting Started

Follow these steps:

### Step 1: Clone the repository

```
git clone https://github.com/yourusername/hangarin.git
cd hangarin
```

### Step 2: Install dependencies

> Use your preferred method to install dependencies

### Step 3: Setup the database

```
python manage.py makemigrations
python manage.py migrate
```

### Step 4: Create a superuser

```
python manage.py createsuperuser
```

### Step 5: Populate with demo data (optional)

```
python manage.py populate_hangarin
```

### Step 6: Run the server

```
python manage.py runserver
```

---

## 🌐 Deployment on PythonAnywhere

1. Push the repo to GitHub.
2. Pull it into PythonAnywhere.
3. Create a virtual environment and install requirements (without specifying pip install here).
4. Update `ALLOWED_HOSTS` and static settings in `settings.py`:

```
ALLOWED_HOSTS = ['yourusername.pythonanywhere.com']
STATIC_ROOT = BASE_DIR / 'staticfiles'
```

5. Run `collectstatic`:

```
python manage.py collectstatic
```

6. Map `/static/` to the `staticfiles` directory in the Web tab.
7. Reload your web app.

---

## 📄 Notes

* Admin panel uses Django’s built-in `LogEntry` model. To hide “Recent Actions”, override the admin index template.
* Use SQLite for development; switch to PostgreSQL in production.

---

## 🗂️ Project Structure

```
hangarin/        # App folder with models, views, templates, etc.
projectsite/     # Django project settings
static/          # Custom CSS/JS files
templates/       # Base and app templates
db.sqlite3       # SQLite database
requirements.txt # Dependencies list
manage.py        # Django management script
```

---
