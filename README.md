# Campus Compass

A comprehensive Django-based web application designed to help students discover and explore educational institutions (colleges and universities) with detailed information about admissions, programs, and campus facilities.

##  Table of Contents

- [Features](#features)
- [Tech Stack](#tech-stack)
- [Installation](#installation)
- [Project Structure](#project-structure)
- [Database Models](#database-models)
- [Usage](#usage)
- [Configuration](#configuration)
- [Contributing](#contributing)
- [License](#license)

##  Features

- **Institution Directory**: Browse and search colleges and universities
- **Detailed Institution Information**: View comprehensive details including:
  - Academic programs and departments
  - Location and nearby hostels
  - Contact information and rankings
  - Photo galleries
  - Application status
- **Admission Circulars**: Stay updated with latest admission announcements and deadlines
- **User Authentication**: Secure user registration and login system
- **User Profiles**: Create and manage personal profiles with bio and contact information
- **Password Management**: Secure password reset functionality
- **Search Functionality**: Search institutions and circulars by keywords
- **Admin Dashboard**: Manage institutions, circulars, users, and content

##  Tech Stack

- **Backend**: Django 5.1.7
- **Database**: SQLite (default)
- **Frontend**: HTML5, CSS3, JavaScript
- **Python Version**: 3.x
- **Additional Libraries**:
  - asgiref (ASGI support)
  - sqlparse (SQL parsing)
  - tzdata (Timezone data)

##  Installation

### Prerequisites
- Python 3.8 or higher
- pip (Python package manager)
- virtualenv (recommended)

### Setup Steps

1. **Clone the repository**
   `bash
   git clone https://github.com/1farha2023/Campus_Compass.git
   cd Campus_Compass
   `

2. **Create and activate virtual environment**
   `bash
   # On Windows
   python -m venv venv
   venv\Scripts\activate

   # On macOS/Linux
   python3 -m venv venv
   source venv/bin/activate
   `

3. **Install dependencies**
   `bash
   pip install -r requirements.txt
   `

4. **Apply database migrations**
   `bash
   python manage.py migrate
   `

5. **Create a superuser (admin account)**
   `bash
   python manage.py createsuperuser
   `

6. **Collect static files**
   `bash
   python manage.py collectstatic
   `

7. **Run the development server**
   `bash
   python manage.py runserver
   `

The application will be available at http://127.0.0.1:8000/

##  Project Structure

Campus_Compass/
 Campus_Compass/          # Main project settings
    settings.py         # Django settings
    urls.py             # URL routing
    wsgi.py             # WSGI configuration
    asgi.py             # ASGI configuration
 CC/                      # Main application
    models.py           # Database models
    views.py            # View logic
    forms.py            # Form definitions
    urls.py             # App URL patterns
    admin.py            # Admin configuration
    signals.py          # Django signals
    migrations/         # Database migrations
 Template/               # HTML templates
    base.html           # Base template
    navbar.html         # Navigation bar
    CC/                 # App-specific templates
 static/                 # Static files (CSS, JS, images)
 media/                  # User-uploaded files
 manage.py              # Django management script
 requirements.txt       # Python dependencies
 README.md             # This file

##  Database Models

### Category
- Categorizes institutions (University, College, etc.)

### InstituteInfo
- Core institution information
- Fields: title, category, description, location, nearby_hostels, rank, department, contact, status

### InstituteImage
- Image gallery for institutions
- Stores multiple images per institution

### Circular
- Admission announcements and notices
- Fields: title, image, admission_period, programs, details, published_date, is_active

### CustomUser
- Extended user model with custom fields
- Inherits from Django's AbstractUser

### Profile
- User profile information
- Fields: bio, phone_number, profile_pic, institute_preference

##  Usage

### For Students
1. Navigate to the home page to browse institutions
2. Click on an institution to view detailed information
3. Check admission circulars for application deadlines
4. Create an account to save preferences
5. Update your profile with personal information

### For Administrators
1. Access admin panel at http://localhost:8000/admin/
2. Login with superuser credentials
3. Manage institutions, circulars, categories, and users
4. View and moderate user profiles

##  Configuration

### Django Settings
- **SECRET_KEY**: Update in Campus_Compass/settings.py for production
- **DEBUG**: Set to False in production
- **ALLOWED_HOSTS**: Configure for your domain
- **DATABASES**: Configure database settings
- **INSTALLED_APPS**: Add custom applications as needed

### Media Files
- User uploads are stored in the media/ directory
- Image validation is configured for specific file types (JPG, JPEG, PNG)

##  Contributing

1. Fork the repository
2. Create a feature branch (git checkout -b feature/AmazingFeature)
3. Commit your changes (git commit -m 'Add some AmazingFeature')
4. Push to the branch (git push origin feature/AmazingFeature)
5. Open a Pull Request

##  License

This project is open source and available under the MIT License.

##  Contact & Support

For issues, questions, or suggestions, please open an issue on the GitHub repository.

---

**Campus Compass** - Navigating Your Educational Journey
