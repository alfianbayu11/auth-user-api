# User Authentication API

This project is a user authentication API built with FastAPI, SQLAlchemy, and JWT for token-based authentication.

## Features

- User registration
- User login
- Protected resource access

## Design Decisions

1. **FastAPI**: Chosen for its high performance and ease of creating quick and efficient APIs.
2. **SQLAlchemy**: Used as an ORM to simplify interactions with the MySQL database, allowing us to write Python code instead of raw SQL.
3. **JWT (JSON Web Token)**: Selected for token-based authentication due to its security and ability to store user information in an encrypted token.

## Library Choices

- **FastAPI**: The main framework for building the API.
- **SQLAlchemy**: ORM for database interactions.
- **passlib**: For secure password hashing.
- **python-jose**: For encoding and decoding JWT.
- **pydantic**: For data validation.

## Challenges

1. **Security**: Ensuring user data is secure during registration and login processes. This was addressed by using secure password hashing and JWT.
2. **Database Integration**: Setting up and migrating the database with SQLAlchemy, ensuring the database schema matches the defined models.
3. **Token Management**: Handling token expiration and ensuring expired tokens cannot be used to access protected resources.

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

