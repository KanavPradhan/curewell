# CureWell Hospital Surgery Management System

## Overview
CureWell is a hospital surgery management system designed to streamline the process of scheduling, managing, and tracking surgeries. It features user authentication, role-based access, and data security.

## Features
- Role-based access control
  - **Doctors**: View and edit surgery details, including timestamps
  - **Patients**: View their surgery-related information only
- Secure authentication and authorization
- REST API for backend operations
- Mobile-responsive frontend

## Tech Stack
- **Backend**: Spring Boot (Java)
- **Frontend**: React.js
- **Database**: MySQL
- **Security**: Spring Security, JWT Authentication
- **Deployment**: Docker, AWS EC2

## Installation
### Backend Setup
1. Clone the repository:
   ```sh
   git clone https://github.com/your-username/curewell.git
   cd curewell/backend
   ```
2. Configure the database connection in `application.properties`.
3. Build and run the application:
   ```sh
   mvn clean install
   mvn spring-boot:run
   ```

### Frontend Setup
1. Navigate to the frontend directory:
   ```sh
   cd frontend
   ```
2. Install dependencies:
   ```sh
   npm install
   ```
3. Run the frontend application:
   ```sh
   npm start
   ```

## API Endpoints
| Method | Endpoint | Role | Description |
|--------|------------|------|-------------|
| GET | /api/surgeries | Doctor, Patient | Fetch all surgeries |
| POST | /api/surgeries | Doctor | Add a new surgery |
| PUT | /api/surgeries/{id} | Doctor | Update surgery details |
| DELETE | /api/surgeries/{id} | Doctor | Remove a surgery |

## Deployment (Docker & AWS EC2)
1. Ensure Docker and AWS CLI are installed.
2. Build and run the backend:
   ```sh
   docker build -t curewell-backend .
   docker run -p 8080:8080 curewell-backend
   ```
3. Build and run the frontend:
   ```sh
   cd frontend
   docker build -t curewell-frontend .
   docker run -p 3000:3000 curewell-frontend
   ```
4. Deploy on AWS EC2 following standard Docker deployment steps.


## Contributors
- Kanav Pradhan - Developer

## Contact
For any issues or suggestions, please raise an issue on GitHub.

