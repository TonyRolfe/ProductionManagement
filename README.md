# ProductionManagement

A Django-based Manufacturing Production Management WebApp for tracking production runs through key stages: machining, assembly, packaging, and heat shrinking.

Originally built for a specific manufacturing workflow (field names reflect that domain), but designed to be adaptable — rename models/fields to fit other production processes.

Open-sourced under the GNU GPL-3.0 license.

## Features

- Track production jobs through sequential stages
- User authentication and role-based views (my jobs, all jobs, active jobs)
- Admin interface for managing production data
- Django Tables 2 for clean tabular displays
- Simple form-driven workflow for starting and advancing jobs

## Tech Stack

- **Backend**: Django (>=2.2)
- **Database**: SQLite (dev) — easily swapped for PostgreSQL/MySQL
- **Frontend**: Django templates + basic HTML/CSS
- **Tables**: django-tables2
- **Other**: pytz, sqlparse

## Project Structure

```
ProductionManagement/
├── ProductionManagementBackend/
│   ├── LaserProductionTracker/   # Main app (models, views, urls, templates)
│   ├── ProductionManagementBackend/  # Project settings, root urls, wsgi
│   ├── templates/
│   ├── manage.py
│   └── db.sqlite3 (dev database)
├── requirements.txt
└── README.md
```

## Quick Start

1. **Clone the repository**
   ```bash
   git clone https://github.com/TonyRolfe/ProductionManagement.git
   cd ProductionManagement/ProductionManagementBackend
   ```

2. **Create and activate a virtual environment**
   ```bash
   python3 -m venv venv
   source venv/bin/activate   # Windows: venv\Scripts\activate
   ```

3. **Install dependencies**
   ```bash
   pip install -r ../requirements.txt
   ```

4. **Run migrations & start the server**
   ```bash
   python manage.py migrate
   python manage.py createsuperuser   # optional, for admin access
   python manage.py runserver
   ```

5. Open http://127.0.0.1:8000/ in your browser.

## Current Status

- Early-stage / proof-of-concept
- Core models, views, and templates for job tracking exist
- Authentication and basic CRUD flows in place
- Needs modernization (Django LTS upgrade, better frontend, tests, Docker, CI)

## Roadmap (Portfolio Polish)

- [ ] Upgrade to modern Django LTS + add type hints where useful
- [ ] Add comprehensive unit/integration tests
- [ ] Dockerize for easy demo deployment
- [ ] Improve UI (Bootstrap or Tailwind)
- [ ] Expand documentation and contribution guide
- [ ] Add example data seeding command

## Contributing

Contributions welcome! Feel free to open issues or PRs. Because this was built around a specific manufacturing process, suggestions for generalization are especially appreciated.

## License

GNU GPL-3.0 — see LICENSE file (or project root) for details.

---

Built by [Tony Rolfe](https://github.com/TonyRolfe) · Portfolio project
