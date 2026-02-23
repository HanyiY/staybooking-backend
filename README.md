# StayBooking Backend Service

A production-style backend service for a short-term stay rental platform.  
This project focuses on backend system design, data modeling, and API correctness rather than UI polish.

## What this project is
- A Spring Boot backend that supports core booking workflows:
    - user roles (host / guest)
    - listing management
    - booking creation and date-based availability
- Designed as a realistic service with persistent storage and clear domain boundaries

## What I worked on
- Designed RESTful APIs and request/response DTOs
- Modeled relational data for users, listings, and bookings
- Implemented core business logic for booking lifecycle and validation
- Built repository and service layers with clear separation of concerns
- Added centralized exception handling for consistent API behavior
- Set up local development with PostgreSQL (optionally via Docker)

## Tech Stack
- Java, Spring Boot
- PostgreSQL
- REST APIs
- Docker (local setup)

## Project Structure (high level)

```text
src/main/java/com/liaoffer/staybooking
├── booking        # booking domain logic
├── listing        # listing domain logic
├── location       # geolocation models
├── repository     # data access layer
├── model / dto    # entities and API contracts
├── storage        # storage-related logic
└── config         # application and security config
```

## Data & Initialization

- Uses PostgreSQL as the primary datastore
- Includes an ApplicationRunner to seed sample data for local development and testing
- Seeded data is intended for demo and development only, not production usage

## How to run locally
1. Start PostgreSQL (locally or via Docker)
2. Configure database connection in `application.yml`
3. Run the application:
   ```bash
   ./gradlew bootRun
   ```

## Design Notes
- Backend-focused by design
- Clear separation between controller, service, and repository layers
- Emphasis on correctness, maintainability, and readable domain logic
- Scoped to demonstrate production-style backend thinking rather than full feature coverage
- Verified end-to-end functionality using Docker-based local setup with PostgreSQL
- Deployed to Google Cloud Run with Java 21 runtime.



## Why I built this
I built this project to practice designing and implementing a backend service end to end, 
similar to what I would work on in a product engineering team, with attention to data modeling, 
API design, and real-world workflows.
