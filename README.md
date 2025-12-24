
# Practice — Django Authentication & Website Project

**practice**

A Django-based website featuring authentication (signup, login, logout), protected pages, account management, and a clean UI with reusable templates and static assets.

---

**📂 Project Structure**
```
practice/
│
├── practice/                # Main project folder
│   ├── settings.py
│   ├── urls.py
│   └── wsgi.py
│
├── code1/                   # Main application
│   ├── migrations/
│   ├── __init__.py
│   ├── admin.py
│   ├── apps.py
│   ├── models.py
│   ├── tests.py
│   ├── urls.py
│   └── views.py
│
├── templates/               # Global templates
│   ├── base.html
│   ├── home.html
│   ├── about.html
│   ├── service.html
│   ├── contact.html
│   ├── login.html
│   ├── signup.html
│   ├── account.html
│   ├── account_sidebar.html
│   ├── settings.html
│   └── change_password.html
│
├── static/                  # Static files
│   └── css/
│       ├── style.css
│       ├── home.css
│       ├── about.css
│       ├── service.css
│       ├── contact.css
│       └── account.css
│
├── db.sqlite3
├── manage.py
├── requirements.txt
└── README.md
```

---

## ⚙️ Features

* User Authentication (Signup, Login, Logout)
* Login-protected pages using `@login_required`
* Account Dashboard
* Change Password (Django built-in form)
* Global Navbar & Footer
* Separate CSS for each page
* Clean template inheritance using `base.html`

---

## 🧠 Code Analysis

### `code1/urls.py`

* Handles routing for all pages
* Clean URL naming for template linking

### `code1/views.py`

* Uses Django authentication system
* `login_required` ensures page protection
* Password change handled securely
* Uses Django messages framework

### Templates

* `base.html` → Layout, navbar, auth-based menu
* Page-specific templates extend base
* Sidebar included using `{% include %}`

### Static Files

* Centralized CSS folder
* Each page loads its own CSS via `{% block extra_css %}`

---

## 🛠️ Setup & Run Locally

### 1️⃣ Clone Repository

```bash
git clone https://github.com/your-username/practice.git
cd practice
```

### 2️⃣ Create Virtual Environment

```bash
python -m venv venv
venv\Scripts\activate  # Windows
source venv/bin/activate # Linux/Mac
```

### 3️⃣ Install Dependencies

```bash
pip install django
```

Create `requirements.txt`

```bash
pip freeze > requirements.txt
```

### 4️⃣ Migrate Database

```bash
python manage.py makemigrations
python manage.py migrate
```

### 5️⃣ Create Superuser (Optional)

```bash
python manage.py createsuperuser
```

### 6️⃣ Run Server

```bash
python manage.py runserver
```

Visit: `http://127.0.0.1:8000/`

---

## 🚀 Future Improvements

* Email verification
* Profile image upload
* Contact form backend
* Deployment (Render / Railway)

---
