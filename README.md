# Nanu Backend

Nanu Backend API for data analysis and storage.

## Project Components

- **Backend**: Built on FastAPI, the backend handles API requests, business logic, and data management.
- **Database**: Utilizes PostgreSQL for secure and reliable data storage.
- **Authentication**: Implements Firebase for robust identity and access management. (In Progress)
- **Migrations**: Manages database changes over time with Alembic.
- **ORM**: Employs SQLAlchemy for database entity mapping.
- **Validation**: Utilizes Pydantic for data validation within FastAPI.
- **Testing**: Uses Pytest for backend testing.

## Getting Started

### Prerequisites

- Docker and Docker Compose
- Python 3.8+ and Poetry (for backend)

### Environment Setup

```bash
git clone https://github.com/theCruxStudios/nanu-backend.git
cd nanu-backend
```

### Running with Docker

```bash
docker-compose up --build
```

This command will build and start the services defined in docker-compose.yml, setting up the backend, redis, and the database.

### Backend Development

The backend API is built using FastAPI and manages interactions with the database.

If you want to run the backend locally instead of through Docker, use Poetry to install and run:

```bash
cd backend
poetry install
poetry run python -m nanu
```

The swagger API documentation is available at `/api/docs` once the server is running.

### Database Migrations with Alembic, example commands:

```bash
alembic revision --autogenerate -m "Your message"
alembic upgrade head
alembic downgrade base
```

Ensure the database service is active before running migrations.

## Testing

### Backend Tests

```bash
cd backend
poetry run pytest
```

## Acknowledgements

- The whole Nanu team.
