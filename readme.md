# FastAPI PostgreSQL Docker Example

This is a simple example project demonstrating how to build a FastAPI application that interacts with a PostgreSQL database using Docker.

## Requirements

- Python 3.7+
- Docker

## Installation

1. Clone the repository:

    ```bash
    git clone https://github.com/eaedk/fastapi-postgresql-docker.git
    ```

2. Navigate to the project directory:

    ```bash
    cd fastapi-postgresql-docker
    ```

3. Install the required Python packages:

    ```bash
    pip install -r requirements.txt
    ```

## Usage

1. Start the PostgreSQL database using Docker Compose:

    ```bash
    docker-compose up -d
    ```

2. Run the FastAPI application:

    ```bash
    uvicorn main:app --reload
    ```

3. Access the FastAPI Swagger documentation:

    Open your web browser and go to [http://localhost:8000/docs](http://localhost:8000/docs).

4. Test the endpoints using cURL or any HTTP client.

## Environment Variables

Environment variables are used to configure the PostgreSQL connection. You can set these variables in a `.env` file located in the project directory.

Example `.env` file:

```
POSTGRES_USER=postgres
POSTGRES_PASSWORD=password
POSTGRES_DB=db
SQLALCHEMY_DATABASE_URL=postgresql://${POSTGRES_USER}:${POSTGRES_PASSWORD}@localhost/${POSTGRES_DB}
```

## Endpoints

- `POST /items/`: Create a new item.
- `GET /items/{item_id}`: Retrieve an item by ID.
- `PUT /items/{item_id}`: Update an existing item.
- `DELETE /items/{item_id}`: Delete an item by ID.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
