# CRM1 Website Django

![Build Status](https://img.shields.io/badge/build-passing-brightgreen)
![License](https://img.shields.io/badge/license-MIT-blue)
![Version](https://img.shields.io/badge/version-1.0.0-blue)

A robust, scalable CRM platform built with Django to manage customer relationships effectively.

## Features

### Scalable API
**What it does:** Provides a RESTful API for managing customers and products.
**Why it exists:** Enables seamless integration with other systems and applications.
**Why it is useful:** Facilitates automation and data exchange.

### User-Friendly Interface
**What it does:** Offers an intuitive and responsive design.
**Why it exists:** Enhances user experience and productivity.
**Why it is useful:** Improves customer satisfaction and reduces training time.

### Secure Authentication
**What it does:** Implements robust authentication and authorization mechanisms.
**Why it exists:** Ensures data security and compliance with regulations.
**Why it is useful:** Protects sensitive information and maintains trust.

### Database Integration
**What it does:** Built-in support for PostgreSQL, a powerful relational database.
**Why it exists:** Provides reliable storage and retrieval of customer data.
**Why it is useful:** Ensures data integrity and scalability.

### Reporting
**What it does:** Generates reports on customer data and interactions.
**Why it exists:** Helps in making informed decisions based on data insights.
**Why it is useful:** Improves business intelligence and decision-making processes.

### Customizable
**What it does:** Easily extendable and customizable to fit specific needs.
**Why it exists:** Allows for flexibility and scalability.
**Why it is useful:** Tailors the platform to meet unique business requirements.

### Automated Tests
**What it does:** Comprehensive test suite to ensure software quality.
**Why it exists:** Reduces bugs and improves reliability.
**Why it is useful:** Ensures that changes do not break existing functionality.

## How It Works

The CRM1 Website Django project is a customer-product management platform built with Django. It includes features such as a RESTful API for customer management, a user-friendly interface, secure authentication, and support for PostgreSQL. The architecture follows the Model-View-Template (MVT) pattern, where:

- **Models** define the data structure.
- **Views** handle business logic and interact with models.
- **Templates** manage the presentation layer.

## Technology Stack

| Technology  | Purpose                           |
|-------------|-----------------------------------|
| Python      | Core programming language         |
| Django      | Web framework                      |
| PostgreSQL  | Database management                |
| Django REST Framework | API development |
| Docker      | Containerization                  |
| Git         | Version control                   |

## Requirements

- Python 3.8+
- PostgreSQL
- Docker (optional, for containerization)

## Installation

### Prerequisites

Ensure you have the following installed:

- Python 3.8+
- PostgreSQL
- Docker (optional)

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

## Configuration

The project uses environment variables for configuration. The `.env` file should contain:

- `DEBUG`: Set to `True` for development, `False` for production.
- `DATABASE_NAME`, `DATABASE_USER`, `DATABASE_PASSWORD`: PostgreSQL database credentials.

## Quick Start

To start the application and access the core API functionalities, a simple interactive session can be initiated:

```python
from src.api import customer_api

# Creating a customer
customer_api.create_customer(name="John Doe", email="john.doe@example.com")

# Fetching customer information
customer = customer_api.get_customer(email="john.doe@example.com")
print(customer)
```

## Usage

To interact with the API, you can use tools like `curl`, Postman, or any other HTTP client. Here are some example commands:

### Creating a Customer

```bash
curl -X POST http://127.0.0.1:8000/api/customers/ \
-H "Content-Type: application/json" \
-d '{"name": "John Doe", "email": "john.doe@example.com"}'
```

### Fetching a Customer

```bash
curl -X GET http://127.0.0.1:8000/api/customers/john.doe@example.com/
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

## Development

The development workflow involves:

1. **Cloning the repository:**
   ```bash
   git clone https://github.com/PartORG/crm1-website-django.git
   cd crm1-website-django
   ```

2. **Setting up a virtual environment:**
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows use `venv\Scripts\activate`
   ```

3. **Installing dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

4. **Running migrations:**
   ```bash
   python src/manage.py migrate
   ```

5. **Starting the development server:**
   ```bash
   python src/manage.py runserver
   ```

## Testing

The project includes a test suite to ensure software quality:

```bash
python src/manage.py test
```

## Limitations

- The project is designed for small to medium-sized businesses.
- It does not include advanced features like real-time notifications or machine learning.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.