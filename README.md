# ReportFlow
# ReportFlow Django Project

This is a Django project for task management, with the ability to submit completion reports and worked hours. It's meant to be used by Admin, SuperAdmin, and Users to manage tasks and track their completion.

## Prerequisites

Before setting up the project, make sure you have the following installed:

- Python 3.x
- pip (Python's package manager)
- Django (If not installed, it will be installed via `requirements.txt`)

## Setup Instructions

1. **Clone the Repository**:
    ```bash
    git clone https://github.com/Arshincv1/ReportFlow.git
    cd ReportFlow
    ```

2. **Create a Virtual Environment** (Optional but recommended):
    - On Windows:
        ```bash
        python -m venv venv
        .\venv\Scripts\activate
        ```
    - On Mac/Linux:
        ```bash
        python3 -m venv venv
        source venv/bin/activate
        ```

3. **Install Dependencies**:
    Run the following command to install all the required dependencies:

    ```bash
    pip install -r requirements.txt
    ```

4. **Set Up Environment Variables**:
    Create a `.env` file in the root directory of the project by copying the **.env.example** file:

    ```bash
    cp .env.example .env
    ```

    The `.env.example` file contains a template for the environment variables. Open the `.env` file and set the following values:

    ```env
    SECRET_KEY=your-secret-key-here
    DEBUG=True
    ```

    **Note**: Replace `your-secret-key-here` with a secure key. You can generate a new secret key using [Django's secret key generator](https://django-secret-key-generator.herokuapp.com/) or use `django.core.management.utils.get_random_secret_key()`.

5. **Run Migrations**:
    After setting up the `.env` file, you need to apply the migrations for the database:

    ```bash
    python manage.py migrate
    ```

6. **Run the Development Server**:
    Finally, start the development server:

    ```bash
    python manage.py runserver
    ```

    Your project will be accessible at [http://127.0.0.1:8000](http://127.0.0.1:8000).

## Usage

- You can create a superuser by running:
    ```bash
    python manage.py createsuperuser
    ```

- Access the Admin Panel via [http://127.0.0.1:8000/admin](http://127.0.0.1:8000/admin).

## Notes

- **Don't commit** your actual `.env` file with sensitive information (like `SECRET_KEY`). It’s added to `.gitignore` to prevent it from being pushed to the repository.
- **.env.example** is committed so others know which environment variables are required. Make sure to copy **.env.example** to **.env** and fill in the appropriate values.

