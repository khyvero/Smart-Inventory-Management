# 🛒 Smart Inventory Management API

## Overview
A backend system for managing warehouse inventory, featuring automated low-stock alerts. This project focuses on solid backend engineering principles, database relations, and scheduled background tasks.

## Tech Stack
*   **Backend:** Java, Spring Boot (Spring Web, Spring Scheduling)
*   **Database:** MySQL or PostgreSQL
*   **Tooling:** Maven/Gradle, Docker

## Features
*   **CRUD Operations:** Endpoints to Create, Read, Update, and Delete products and categories.
*   **Relational Mapping:** One-to-Many relationship between `Category` and `Product`.
*   **Scheduled Jobs:** A Spring `@Scheduled` task that runs every minute to check for products where `quantity < threshold` and logs an alert.
*   **Data Validation:** Ensure price is always positive and SKUs are unique using Spring Boot Validation.

## Development Tasks (To-Do)
- [ ] Set up the Spring Boot application and define entities (`Product`, `Category`).
- [ ] Implement global exception handling (e.g., returning proper 404s for 'Product Not Found').
- [ ] Implement the `@Scheduled` low-stock alert service.
- [ ] Containerize the application using a multi-stage `Dockerfile`.
- [ ] Provide a `docker-compose.yml` to launch the app and the database with initialized dummy data.

## Getting Started
1. Configure your `.env` file with database credentials.
2. Run `docker-compose up -d` to start the database.
3. Run the application via IntelliJ or your preferred IDE.
