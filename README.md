# CRM1 Website Django

![Build Status](https://img.shields.io/badge/build-passing-brightgreen)
![License](https://img.shields.io/badge/license-MIT-blue)
![Version](https://img.shields.io/badge/version-1.0.0-blue)

A robust, scalable CRM platform built with Django to manage customer relationships effectively.

## Features

- 🔧 **Scalable API**: RESTful API for customer management.
- 🎨 **User-Friendly Interface**: Responsive design for improved user experience.
- 🔒 **Secure Authentication**: Implement robust authentication and authorization.
- 🗃️ **Database Integration**: Built-in support for PostgreSQL.
- 📊 **Reporting**: Generate reports on customer data and interactions.
- ⚙️ **Customizable**: Easily extendable and customizable to fit specific needs.
- 🛠️ **Automated Tests**: Comprehensive test suite to ensure software quality.

## Tech Stack

| Technology  | Purpose                           |
|-------------|-----------------------------------|
| Python      | Core programming language         |
| Django      | Web framework                      |
| PostgreSQL  | Database management                |
| Django REST Framework | API development |
| Docker      | Containerization                  |
| Git         | Version control                   |

## Quick Start

### Prerequisites

- Python 3.8+
- PostgreSQL
- Docker (optional, for containerization)

### Installation Steps

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
   python src/manage.py migrate
   ```

5. **Start the server:**

   ```bash
   python src/manage.py runserver
   ```

## Usage

To start the application and access the core API functionalities, a simple interactive session can be initiated:

```python
from src.api import customer_api

# Creating a customer
customer_api.create_customer(name="John Doe", email="john.doe@example.com")

# Fetching customer information
customer = customer_api.get_customer(email="john.doe@example.com")
print(customer)
```

## Project Structure

```plaintext
crm1-website-django/
├── src/
│   ├── main.py                 # Entry point for the application
│   ├── api/                    # API endpoints
│   └── models/                 # Database models
├── tests/                      # Test cases
├── requirements.txt            # Dependency list
├── setup.py                    # Package setup
├── README.md                   # Project documentation
└── .env                        # Environment variables
```

## API Reference

For detailed documentation on each API endpoint, refer to [API Reference](src/api/README.md).

## Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository
2. Create a branch (`git checkout -b feature/your-feature-name`)
3. Commit your changes (`git commit -am 'Add new feature'`)
4. Push to the branch (`git push origin feature/your-feature-name`)
5. Open a Pull Request

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
