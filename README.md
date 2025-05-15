# ALX Travel App

![Django](https://img.shields.io/badge/Django-092E20?style=for-the-badge&logo=django&logoColor=white)
![DRF](https://img.shields.io/badge/django%20rest-ff1709?style=for-the-badge&logo=django&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-005C84?style=for-the-badge&logo=mysql&logoColor=white)
![Swagger](https://img.shields.io/badge/Swagger-85EA2D?style=for-the-badge&logo=Swagger&logoColor=white)

A comprehensive travel application built with Django REST Framework that provides listings of travel destinations, accommodations, and activities.

## Features

- **RESTful API** built with Django REST Framework
- **MySQL Database** for reliable data storage
- **Swagger Documentation** for easy API exploration
- **CORS Support** for cross-origin requests
- **Environment Variables** for secure configuration
- **Celery Integration** for asynchronous task processing

## Prerequisites

- Python 3.8+
- MySQL 5.7+
- Redis or RabbitMQ (for Celery tasks)

## Installation

1. **Clone the repository**
```bash
 git clone https://github.com/heba-webdev/alx_travel_app.git
   cd alx_travel_app
```

2. **Set up virtual environment**
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

3. **Install dependencies**
```bash
pip install -r requirements.txt
```

4. **Configure environment variables**
   
- Create a .env file in the project root

- Add your configuration (see example below)

```bash
Example .env file:
DEBUG=True
SECRET_KEY=your-secret-key-here
DB_NAME=alx_travel_db
DB_USER=root
DB_PASSWORD=yourpassword
DB_HOST=localhost
DB_PORT=3306
```

5. **Set up database**
   
- Create a MySQL database

- Update the .env file with your database credentials

7. **Run migrations**
```bash
python manage.py migrate
```

### Running the Application

```bash
celery -A alx_travel_app worker -l info
```

## Project Structure

```bash
alx_travel_app/
├── alx_travel_app/          # Project configuration
│   ├── settings.py           # Django settings
│   ├── urls.py               # Main URLs
│   └── ...
├── listings/                 # Travel listings app
│   ├── migrations/           # Database migrations
│   ├── models.py             # Data models
│   ├── views.py              # API views
│   ├── serializers.py        # Data serializers
│   └── urls.py               # App URLs
├── .env                      # Environment variables
├── requirements.txt          # Dependencies
└── manage.py                 # Django management script
```