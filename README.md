﻿# User Authentication API

This project is a user authentication API built with FastAPI, SQLAlchemy, and JWT for token-based authentication.

## Features

- User registration
- User login
- Protected resource access

## Setup

### Prerequisites

- Python 3.7+
- MySQL

### Installation

1. Clone the repository:

    ```bash
    git clone https://github.com/alfianbayu11/auth-user-api.git
    cd auth-user-api
    ```

2. Create a virtual environment and activate it:

    ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows use `venv\Scripts\activate`
    ```

3. Install the dependencies:

    ```bash
    pip install -r requirements.txt
    ```

4. Set up the database:

    ```bash
    # Update the database URL in `database.py` if necessary
    python main.py
    ```

## Usage

1. Run the application:

    ```bash
    uvicorn main:app --reload
    ```

2. The API will be available at `http://127.0.0.1:8000`.

## Endpoints

- `POST /register`: Register a new user
- `POST /login`: Login and get an access token
- `GET /get-resource`: Access a protected resource (requires token)

## Configuration

- `SECRET_KEY`: Change this to a strong secret key
- `ACCESS_TOKEN_EXPIRE_MINUTES`: Set the token expiration time

## License

This project is licensed under the MIT License.

