# stat-ng

StatNG has the goal of overhauling the current data infrastructure in Nigeria.

Technologies: Flask, SQlite

statng/
├── app/                         # Core Flask application package
│   ├── __init__.py              # App factory & extension setup
│   ├── config.py                # App config (dev/prod)
│   ├── models/                  # SQLAlchemy models (User, Dataset, etc.)
│   ├── routes/                  # Jinja-based route views (HTML)
│   ├── api/                     # JSON APIs for frontend (data, auth)
│   ├── templates/               # HTML templates (Jinja2)
│   ├── static/                  # Static assets: JS, CSS, images
│   ├── forms/                   # WTForms (login, upload)
│   ├── utils/                   # Data processing, validation functions
│   └── services/                # Optional scraping/NLP modules
│
├── instance/                    # Local SQLite DB lives here (if needed)
│   └── statng.db
│
├── data/                        # Test/sample datasets
│   ├── dummy_health.csv
│   └── dummy_education.csv
│
├── tests/                       # Unit & integration tests
│   ├── test_auth.py
│   └── test_data_api.py
│
├── migrations/                  # Flask-Migrate directory (Alembic)
├── .env                         # Environment variables (secret keys, DB URL)
├── run.py                       # Entry point to launch the app
├── requirements.txt             # Project dependencies
├── README.md                    # Project overview and usage
├── statng_tasks.csv             # (Optional) CSV for task tracking

