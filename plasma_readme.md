# Plasma Providing System

A comprehensive blood bank management system built with Django to streamline plasma and blood donation processes, donor management, and patient services.

## 🩸 Features

- **Blood Bank Management**: Complete administration of blood inventory and operations
- **Donor Management**: Registration, profile management, and donation tracking for blood donors
- **Patient Services**: Patient registration, blood request management, and medical records
- **Admin Dashboard**: Comprehensive admin interface for system management
- **Responsive Design**: Mobile-friendly interface for all user types

## 🛠️ Tech Stack

- **Backend**: Python Django
- **Frontend**: HTML, CSS
- **Database**: SQLite3
- **Web Server**: Django Development Server

## 📁 Project Structure

```
plasma-providing-system/
├── blood/                      # Main blood bank app
│   ├── admin.py               # Admin interface configurations
│   ├── apps.py                # App configuration
│   ├── forms.py               # Forms for blood-related operations
│   ├── models.py              # Database models for blood management
│   ├── tests.py               # Unit tests
│   ├── views.py               # View functions and classes
│   └── __init__.py
├── bloodbank/                  # Main project directory
│   ├── asgi.py                # ASGI configuration
│   ├── settings.py            # Django settings
│   ├── urls.py                # Main URL configuration
│   └── wsgi.py                # WSGI configuration
├── donor/                      # Donor management app
│   ├── urls.py                # Donor-specific URLs
│   ├── admin.py               # Donor admin interface
│   ├── apps.py                # App configuration
│   ├── forms.py               # Donor registration and management forms
│   ├── models.py              # Donor database models
│   ├── tests.py               # Unit tests
│   ├── views.py               # Donor-related views
│   └── __init__.py
├── patient/                    # Patient management app
│   ├── urls.py                # Patient-specific URLs
│   ├── admin.py               # Patient admin interface
│   ├── apps.py                # App configuration
│   ├── forms.py               # Patient registration and request forms
│   ├── models.py              # Patient database models
│   ├── tests.py               # Unit tests
│   ├── views.py               # Patient-related views
│   └── __init__.py
├── static/                     # Static files
│   ├── css/                   # Stylesheets
│   └── images/                # Image assets
├── templates/                  # HTML templates
│   ├── blood/                 # Blood management templates
│   ├── donor/                 # Donor interface templates
│   └── patient/               # Patient interface templates
├── db.sqlite3                  # SQLite database file
├── manage.py                   # Django management script
└── requirements.txt            # Python dependencies
```

## 🚀 Installation & Setup

### Prerequisites

- Python 3.8 or higher
- pip (Python package manager)

### Step-by-Step Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/plasma-providing-system.git
   cd plasma-providing-system
   ```

2. **Create a virtual environment**
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

4. **Run database migrations**
   ```bash
   python manage.py makemigrations
   python manage.py migrate
   ```

5. **Create a superuser account**
   ```bash
   python manage.py createsuperuser
   ```

6. **Start the development server**
   ```bash
   python manage.py runserver
   ```

7. **Access the application**
   - Main application: `http://127.0.0.1:8000/`
   - Admin panel: `http://127.0.0.1:8000/admin/`

## 📋 Usage

### For Administrators
- Access the admin panel to manage blood inventory, donors, and patients
- Monitor donation activities and blood requests
- Generate reports and maintain system records

### For Donors
- Register as a new donor
- Update personal information and medical history
- View donation history and schedule appointments
- Check eligibility for blood donation

### For Patients
- Register for blood requests
- Submit blood requirement requests
- Track request status
- View medical records and donation history

## 🔧 Configuration

### Database Settings
The application uses SQLite3 by default. To modify database settings, edit `bloodbank/settings.py`:

```python
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.sqlite3',
        'NAME': BASE_DIR / 'db.sqlite3',
    }
}
```

### Static Files
Static files are served from the `static/` directory. In production, configure your web server to serve these files directly.

## 🧪 Testing

Run the test suite to ensure everything works correctly:

```bash
python manage.py test
```

Run tests for specific apps:
```bash
python manage.py test blood
python manage.py test donor
python manage.py test patient
```

## 📝 API Endpoints

The application provides the following main URL patterns:

- `/` - Home page
- `/blood/` - Blood management interface
- `/donor/` - Donor registration and management
- `/patient/` - Patient services and requests
- `/admin/` - Administrative interface

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/new-feature`)
3. Commit your changes (`git commit -am 'Add new feature'`)
4. Push to the branch (`git push origin feature/new-feature`)
5. Create a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🆘 Support

For support and questions:
- Create an issue in the GitHub repository
- Contact the development team

## 🔮 Future Enhancements

- Mobile application integration
- Advanced reporting and analytics
- Email notifications for donors and patients
- Integration with hospital management systems
- Multi-language support
- Enhanced security features

---

**Note**: This is a development version. For production deployment, ensure proper security configurations, environment variables, and production-grade database setup.