# URL Shortener using Django

A simple and fast URL shortener web application built with Django that converts long URLs into shorter, more manageable links using the TinyURL service.

## Features

- **URL Shortening**: Convert long URLs to short links using TinyURL service
- **Responsive Design**: Bootstrap-based UI with gradient styling
- **One-Click Copy**: Copy shortened URLs to clipboard with ClipboardJS
- **Form Validation**: Input validation with user-friendly error messages
- **Modern UI**: SweetAlert2 modals for notifications and feedback

## Technology Stack

- **Backend**: Django 5.1.1
- **URL Shortening**: pyshorteners 1.0.1 (TinyURL integration)
- **Frontend**: Bootstrap 5.3.3, SweetAlert2, ClipboardJS
- **Database**: SQLite (default)
- **Deployment**: WSGI/ASGI compatible

## Installation

### Prerequisites
- Python 3.x
- pip (Python package installer)

### Setup Instructions

1. **Create project directory**
   ```bash
   mkdir url-shortener-project
   cd url-shortener-project
   ```

2. **Create and activate virtual environment**
   
   Install virtualenv:
   ```bash
   pip install virtualenv
   ```
   
   Create virtual environment:
   ```bash
   # Windows
   python -m venv venv
   
   # Mac/Linux
   python3 -m venv venv
   ```
   
   Activate virtual environment:
   ```bash
   # Windows
   source venv/scripts/activate
   
   # Mac/Linux
   source venv/bin/activate
   ```

3. **Clone the repository**
   ```bash
   git clone https://github.com/RyomenPanda/URL-Shortener-Django.git
   cd URL-Shortener-Django
   ```

4. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

5. **Run the development server**
   ```bash
   # Windows
   python manage.py runserver
   
   # Mac/Linux
   python3 manage.py runserver
   ```

6. **Access the application**
   Open your browser and navigate to `http://127.0.0.1:8000/`

## Usage

1. Enter a long URL in the input field
2. Click "Submit" to generate a shortened URL
3. Copy the shortened URL using the "Copy" button
4. Share your shortened link!

## Project Structure

```
URL-Shortener-Django/
├── manage.py                 # Django management script
├── requirements.txt          # Python dependencies
├── templates/
│   └── home.html            # Main UI template
└── url_shortener/
    ├── __init__.py
    ├── settings.py          # Django configuration
    ├── urls.py              # URL routing
    ├── views.py             # View logic
    ├── forms.py             # Form definitions
    ├── wsgi.py              # WSGI deployment
    └── asgi.py              # ASGI deployment
```

## Key Components

- **`Urlgenerate` View**: Main FormView handling URL shortening requests
- **`UrlForm`**: Django form for URL input validation
- **TinyURL Integration**: Uses pyshorteners library for URL shortening
- **Responsive Template**: Bootstrap-styled interface with copy functionality

## Deployment

The application supports both WSGI and ASGI deployment:

- **WSGI**: Use `url_shortener/wsgi.py` for traditional deployment
- **ASGI**: Use `url_shortener/asgi.py` for asynchronous deployment

### Production Deployment
1. Set `DEBUG = False` in settings.py
2. Configure allowed hosts
3. Set up static file serving
4. Use a production WSGI/ASGI server (Gunicorn, uWSGI, etc.)

## Dependencies

- Django 5.1.1 - Web framework
- pyshorteners 1.0.1 - URL shortening service integration
- requests 2.32.3 - HTTP library
- pyperclip 1.9.0 - Clipboard operations

## Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Submit a pull request

## License

This project is open source. Feel free to use and modify as needed.

## Author

**Ryomen Panda**
- GitHub: [@RyomenPanda](https://github.com/RyomenPanda)

## Support

If you encounter any issues or have questions, please open an issue on the GitHub repository.
