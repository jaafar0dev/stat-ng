# stat-ng

StatNG has the goal of overhauling the current data infrastructure in Nigeria.

Technologies: Flask, SQlite

statng/
├── app/ # Core Flask application
│ ├── **init**.py # App factory, init extensions (Flask, DB)
│ ├── config.py # Config settings (dev/prod/keys)
│ ├── models/ # SQLAlchemy models
│ │ └── user.py # User model (admin, orgs)
│ │ └── dataset.py # Dataset + metadata
│ ├── routes/ # All views/routes (Jinja templates)
│ │ └── main.py # Home & dashboard routes
│ │ └── auth.py # Login/signup/logout routes
│ │ └── admin.py # Dataset upload, admin panel
│ ├── api/ # JSON APIs for AJAX & frontend use
│ │ └── data_api.py # GET/POST data for charts
│ │ └── auth_api.py # Login/signup API
│ ├── templates/ # Jinja2 HTML templates
│ │ └── layout.html # Base layout
│ │ └── index.html # Landing page
│ │ └── dashboard.html # Main data dashboard
│ │ └── login.html # Auth pages
│ │ └── admin_upload.html # Admin dataset upload UI
│ ├── static/ # Static assets
│ │ ├── css/
│ │ ├── js/
│ │ │ └── charts.js # Chart rendering scripts
│ │ └── images/
│ ├── forms/ # WTForms or form validation logic
│ │ └── login_form.py
│ │ └── upload_form.py
│ ├── utils/ # Utility functions, processing, validation
│ │ └── data_cleaner.py # Cleans CSVs
│ │ └── chart_helpers.py # Prepares datasets for charts
│ └── services/ # Optional: scraping, AI modules
│ └── scr
