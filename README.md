# CRM1 Website Django

A customer-product management website created in Python/Django.

## Requirements

- Python 3.8+
- PostgreSQL
- asgiref==3.2.7
- boto3==1.14.20
- botocore==1.17.20
- certifi==2020.4.5.1
- Django==3.0.7
- django-filter==2.3.0
- django-storages==1.9.1
- djangorestframework==3.11.0
- docutils==0.15.2
- gunicorn==20.0.4
- jmespath==0.10.0
- Pillow==7.1.2
- psycopg2==2.8.5
- python-dateutil==2.8.1
- pytz==2020.1
- s3transfer==0.3.3
- six==1.15.0
- sqlparse==0.3.1
- urllib3==1.25.9
- whitenoise==5.1.0
- wincertstore==0.2

## Installation

1. **Clone the repository:**

   ```bash
   git clone https://github.com/PartORG/crm1-website-django.git
   cd crm1-website-django
   ```

2. **Install dependencies:**

   ```bash
   pip install -r requirements.txt
   ```

3. **Setup the environment:**

   Create a `.env` file in the root directory with your environment variables:

   ```dotenv
   DEBUG=True
   DATABASE_NAME=your_db_name
   DATABASE_USER=your_db_user
   DATABASE_PASSWORD=your_db_password
   ```

4. **Run Migrations:**

   ```bash
   python manage.py migrate
   ```

5. **Start the server:**

   ```bash
   python manage.py runserver
   ```

## Usage

To start the application and access the core functionalities, use the following command:

```bash
python manage.py runserver
```

This will start the Django development server on `http://127.0.0.1:8000/`. You can then navigate to this URL in your web browser to interact with the CRM platform.

## Project Structure

```plaintext
crm1-website-django/
├── manage.py
├── accounts/
│   ├── __init__.py
│   ├── admin.py
│   ├── apps.py
│   ├── decorators.py
│   ├── filters.py
│   ├── forms.py
│   ├── migrations/
│   ├── models.py
│   ├── signals.py
│   ├── templates/
│   │   └── accounts/
│   │       ├── account_settings.html
│   │       ├── customer.html
│   │       ├── dashboard.html
│   │       ├── delete.html
│   │       ├── login.html
│   │       ├── main.html
│   │       ├── navbar.html
│   │       ├── order_form.html
│   │       ├── password_reset.html
│   │       ├── password_reset_done.html
│   │       ├── password_reset_form.html
│   │       ├── password_reset_sent.html
│   │       ├── products.html
│   │       ├── register.html
│   │       └── status.html
│   ├── tests.py
│   ├── urls.py
│   └── views.py
├── crm1/
│   ├── __init__.py
│   ├── asgi.py
│   ├── settings.py
│   ├── urls.py
│   └── wsgi.py
└── requirements.txt
```

## Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository
2. Create a branch (`git checkout -b feature/your-feature-name`)
3. Commit your changes (`git commit -am 'Add new feature'`)
4. Push to the branch (`git push origin feature/your-feature-name`)
5. Open a Pull Request

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.