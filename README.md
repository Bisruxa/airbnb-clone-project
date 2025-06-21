# airbnb-clone-project
# Airbnb Clone Project

## Project Overview

The Airbnb Clone project is a full-stack web application that replicates the core features of the Airbnb platform. The main goal is to gain hands-on experience with backend and frontend technologies by building a real-world application. The project emphasizes teamwork, agile development practices, secure API design, and modern CI/CD pipelines.

## Team Roles

### 1. Backend Developer
Responsible for building and maintaining the application server, handling routing, data processing, and API design. Works closely with the database and ensures business logic is implemented correctly.

### 2. Frontend Developer
Creates the user interface using modern web frameworks. Works on rendering property listings, booking pages, user dashboards, and handling API calls from the frontend.

### 3. Database Administrator (DBA)
Designs and maintains the database schema. Ensures efficient data storage, indexing, and relationships between tables/entities.

### 4. DevOps Engineer
Sets up and manages the CI/CD pipelines, monitors deployments, manages Docker and cloud resources, and ensures seamless integration from development to production.

### 5. Project Manager
Coordinates the project workflow, organizes tasks using tools like Trello or Jira, monitors deadlines, and facilitates team collaboration.

## Technology Stack

- **Django**: A high-level Python web framework used to build robust backend logic and RESTful/GraphQL APIs.
- **PostgreSQL**: A powerful open-source relational database for storing structured application data.
- **GraphQL**: A query language for APIs used to fetch and update data more efficiently and flexibly than REST.
- **React.js (optional)**: For building the frontend user interface.
- **Docker**: Containerization platform for building consistent development and production environments.
- **GitHub Actions**: Used for setting up CI/CD pipelines that automate testing and deployment.

## Database Design

### Key Entities and Fields

1. **User**
   - `id`
   - `name`
   - `email`
   - `password`
   - `role` (guest or host)

2. **Property**
   - `id`
   - `title`
   - `location`
   - `price_per_night`
   - `host_id` (foreign key to User)

3. **Booking**
   - `id`
   - `property_id` (foreign key)
   - `user_id` (foreign key)
   - `check_in`
   - `check_out`

4. **Review**
   - `id`
   - `property_id` (foreign key)
   - `user_id` (foreign key)
   - `rating`
   - `comment`

5. **Payment**
   - `id`
   - `booking_id` (foreign key)
   - `amount`
   - `status`

### Entity Relationships
- A user can list multiple properties (if they are a host).
- A booking is linked to one property and one user.
- Reviews are submitted by users for specific properties.
- Each booking has one payment record associated with it.

## Feature Breakdown

### User Management
Handles user registration, login, and profile management. Users can act as guests or hosts.

### Property Management
Allows hosts to add, update, and delete property listings, including uploading photos and setting pricing.

### Booking System
Guests can search, book properties, view availability, and manage reservations.

### Review System
Guests can leave feedback after staying at a property, helping others make informed choices.

### Payment Integration
Processes transactions securely using payment gateways, handles receipts, and confirms booking upon successful payment.


## API Security

### Key Security Measures

- **Authentication**: Ensures users are who they claim to be, using token-based authentication (e.g., JWT).
- **Authorization**: Restricts access to specific routes based on user roles (host vs guest).
- **Rate Limiting**: Protects the API from abuse by limiting the number of requests per user.
- **Data Validation**: Prevents SQL injection, XSS, and other input-based attacks.

### Importance
- Protects sensitive user data like emails and passwords.
- Secures the booking and payment processes from unauthorized access.
- Ensures the integrity and reliability of the platform.


## CI/CD Pipeline

### What is CI/CD?
CI/CD stands for Continuous Integration and Continuous Deployment. It's a process that automates building, testing, and deploying code whenever a change is made.

### Tools and Implementation
- **GitHub Actions**: Automates tests and builds on each push.
- **Docker**: Ensures consistency across development, testing, and production environments.
- **Heroku/Vercel/AWS**: Can be used for final deployment of backend/frontend.

CI/CD ensures faster, safer, and more reliable software delivery.

## Manual Review

This README includes all required sections: team roles, tech stack, database design, feature breakdown, API security, and CI/CD pipeline. Further updates and project progress will be documented in this repository.

