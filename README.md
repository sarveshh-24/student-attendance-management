# Student Attendance Management System

A full-stack web application for managing student attendance through separate student and teacher interfaces.

## Overview

The Student Attendance Management System provides a centralized platform for recording, viewing, and managing attendance information.

The application includes role-based access for students and teachers, secure authentication using JWT, and a REST-based backend connected to a database.

## Features

* Student and teacher login
* Role-based access and navigation
* JWT-based authentication
* Password protection using bcrypt
* Student attendance tracking
* Teacher attendance management
* Attendance records and status updates
* REST API for frontend-backend communication
* Responsive user interface
* Persistent authentication using browser local storage

## Tech Stack

### Frontend

* React
* React Router
* Tailwind CSS
* Vite
* JavaScript

### Backend

* Node.js
* Express.js
* MongoDB
* Mongoose
* JSON Web Token (JWT)
* bcrypt

### Development & Deployment

* Git
* GitHub
* Docker
* GitHub Actions

## Project Structure

```text
student-attendance-management/
│
├── client/
│   ├── public/
│   ├── src/
│   │   ├── assets/
│   │   ├── components/
│   │   ├── pages/
│   │   └── ...
│   ├── package.json
│   └── ...
│
├── server/
│   ├── controllers/
│   ├── models/
│   ├── routes/
│   ├── middleware/
│   ├── package.json
│   └── ...
│
├── .github/
│   └── workflows/
│
├── package.json
├── package-lock.json
└── README.md
```

## Authentication

The application uses JWT-based authentication.

During login, the backend validates the supplied credentials and returns a JSON Web Token. The frontend stores the token locally and uses the authenticated session to provide access to the appropriate student or teacher interface.

Passwords are handled using bcrypt rather than being stored directly in plain text.

## Getting Started

### Prerequisites

Make sure the following are installed:

* Node.js
* npm
* MongoDB

### 1. Clone the Repository

```bash
git clone YOUR_REPOSITORY_URL
cd student-attendance-management
```

### 2. Install Dependencies

Install the root dependencies:

```bash
npm install
```

Then install the client dependencies:

```bash
cd client
npm install
```

Install the server dependencies:

```bash
cd ../server
npm install
```

### 3. Configure Environment Variables

Create the required environment files for the client and server.

The exact variables depend on your local database and deployment configuration.

Do not commit sensitive values such as:

* Database connection strings
* JWT secrets
* API keys
* Production credentials

### 4. Start the Application

Start the backend from the `server` directory:

```bash
npm start
```

Start the frontend from the `client` directory:

```bash
npm run dev
```

The frontend will then be available through the local Vite development server.

## API Communication

The frontend communicates with the Express backend through the API URL configured using the Vite environment variable:

```text
VITE_API_URL
```

This keeps the frontend independent of a hard-coded backend address and allows the API endpoint to be changed for different environments.

## User Roles

### Student

Students can log in using their student credentials and access the features available to their role, including viewing attendance information.

### Teacher

Teachers can log in through the teacher interface and manage attendance-related information for students.

## Security Considerations

* Authentication is handled using JWT.
* Passwords are protected using bcrypt hashing.
* Sensitive configuration values should be stored in environment variables.
* Environment files containing secrets should not be committed to the repository.
* Authentication tokens are required for protected application functionality.

## Future Improvements

Possible improvements include:

* Attendance analytics and visual reports
* Exporting attendance records
* Improved form validation
* Password reset functionality
* Email notifications
* More granular role and permission management
* Improved automated testing
* Enhanced deployment monitoring

## License

This project is intended for educational and portfolio purposes.

---

**Student Attendance Management System**
Full-stack web application built with React, Node.js, Express, and MongoDB.
