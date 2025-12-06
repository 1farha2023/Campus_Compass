# Campus Compass

About
-----

Campus Compass is a Django-based web application for discovering and managing information about colleges and universities. It provides features for browsing institutes, viewing institute details, creating and managing circulars, user profiles, and authentication flows.

Key Features
--
- Browse universities and colleges
- Institute detail pages with images and info
- User profiles with profile pictures
- Create and manage circulars (announcements)
- Password reset and authentication flows

Quick Start
--
1. Create and activate a Python virtual environment (recommended):

	```powershell
	python -m venv .venv
	.\.venv\Scripts\Activate.ps1
	pip install -r requirements.txt
	```

2. Apply migrations and create a superuser:

	```powershell
	python manage.py migrate
	python manage.py createsuperuser
	```

3. Run the development server:

	```powershell
	python manage.py runserver
	```

Media and static files
--
- Uploaded media is stored in the `media/` directory.
- Static assets are in `static/` and `staticfiles/` for collected files.

Notes
--
- This repository includes SQLite for local development (`db.sqlite3`). For production, switch to a production-grade database and configure static/media storage appropriately.

License
--
This project does not include a license file. Add one if you plan to publish it publicly.

Contact
--
Maintainer: repository owner
