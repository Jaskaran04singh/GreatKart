# GreatKart - E-Commerce Web Application 🛒

GreatKart is a modern, full-featured e-commerce platform built with Python and Django. It features a custom user authentication model, dynamic category and product catalog management, category-based filtering, and responsive frontend templates.

---

## 🚀 Features Implemented

- **Custom User Authentication (`accounts` app)**:
  - Built with Django's `AbstractBaseUser` and `BaseUserManager`.
  - Email-based authentication instead of standard usernames.
  - Custom `AccountAdmin` interface in Django Admin.
  - Support for superusers, staff permissions, and active status.

- **Categories System (`category` app)**:
  - `Category` model with custom image uploads (`photos/categories`).
  - Automated slug generation with `prepopulated_fields` in Django Admin.

- **Store & Product Catalog (`store` app)**:
  - `Product` model tracking price, stock, availability, and high-resolution images (`photos/products`).
  - Dynamic product listing on the store page.
  - Category-based product filtering (`/store/<category_slug>/`).
  - Active product count and status checks (`is_available`).

- **Frontend & Templates**:
  - Modular Django template structure (`base.html`, `navbar.html`, `footer.html`).
  - Responsive design using Bootstrap 4 and FontAwesome 5.
  - Dynamic homepage and store catalog templates.

- **Media & File Handling**:
  - Image handling with **Pillow**.
  - Configured `MEDIA_URL` and `MEDIA_ROOT` for media uploads.

---

## 🛠️ Tech Stack

- **Backend**: Python 3.13+, Django 6.x
- **Database**: SQLite (Development)
- **Frontend**: HTML5, CSS3, JavaScript, Bootstrap 4, FontAwesome 5
- **Image Processing**: Pillow

---

## 📁 Project Structure

```text
GreatKart/
├── accounts/               # Custom user management & authentication
│   ├── models.py           # Account & MyAccountManager
│   └── admin.py            # Custom UserAdmin
├── category/               # Product category management
│   ├── models.py           # Category model
│   └── admin.py            # CategoryAdmin with auto-slugs
├── store/                  # Products & Store logic
│   ├── models.py           # Product model
│   ├── views.py            # Store & category filtering views
│   └── urls.py             # Store routing
├── greatkart/              # Project settings & root routing
│   ├── settings.py
│   ├── urls.py
│   └── views.py
├── templates/              # HTML Templates
│   ├── base.html
│   ├── home.html
│   ├── includes/           # Navbar & Footer partials
│   └── store/              # Store template
└── static/                 # Static assets (CSS, JS, Images, Fonts)
```

---

## ⚙️ Getting Started

### 1. Clone the repository
```bash
git clone https://github.com/Jaskaran04singh/GreatKart.git
cd GreatKart
```

### 2. Create and activate virtual environment
```bash
# Windows
python -m venv .venv
.venv\Scripts\activate

# macOS / Linux
python3 -m venv .venv
source .venv/bin/activate
```

### 3. Install dependencies
```bash
pip install django pillow
```

### 4. Apply database migrations
```bash
python manage.py migrate
```

### 5. Create a superuser (admin access)
```bash
python manage.py createsuperuser
```

### 6. Start the development server
```bash
python manage.py runserver
```

Open [http://127.0.0.1:8000/](http://127.0.0.1:8000/) in your browser to view the application.
Access the admin panel at [http://127.0.0.1:8000/admin/](http://127.0.0.1:8000/admin/).