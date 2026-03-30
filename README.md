# Event Management System (EMS)

## Description

A backend application for managing events, bookings, and users. This Event Management System provides RESTful APIs for creating and managing events, handling user bookings with ticket availability checks, and retrieving booking information. Built with Node.js, Express.js, and Sequelize ORM for MySQL database integration.

### Key Features
- Event creation and management
- User booking system with ticket validation
- Pagination support for large datasets
- Input validation and error handling
- Transaction-based booking to ensure data consistency
- CORS enabled for cross-origin requests

## Table of Contents
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Usage](#usage)
- [API Endpoints](#api-endpoints)
- [Technologies Used](#technologies-used)
- [Project Structure](#project-structure)
- [Live Url](#live-url)
- 

## Prerequisites

Before running this application, make sure you have the following installed:

- Node.js (v14.0.0 or higher)
- npm (v6.0.0 or higher)
- MySQL database

## Installation

1. **Clone the repository:**
   ```bash
   git clone https://github.com/Atif-1/EMS_Development.git
   ```

2. **Install dependencies:**
   ```bash
   npm install
   ```

3. **Set up environment variables:**
   Create a `.env` file in the root directory with the following variables:
   ```
   PORT=3000
   DB_HOST=localhost
   DB_USER=your_mysql_username
   DB_PASSWORD=your_mysql_password
   DB_NAME=event_management_db
   ```

4. **Set up the database:**
   - Create a MySQL database named `event_management_db`
   - The application will automatically create tables using Sequelize migrations

5. **Start the server:**
   ```bash
   npm start
   ```

   The server will start on the port specified in your `.env` file (default: 3000).

## Usage

Once the server is running, you can interact with the API using tools like Postman.

### API Documentation

For detailed API documentation, refer to the `documentation/ems.yaml` file, which contains the OpenAPI 3.0 specification. You can import this file into Swagger UI for interactive API documentation.

## API Endpoints

- `GET /events` - Retrieve all events
- `POST /events` - Create a new event
- `POST /events/{id}/attendance` - Get bookings for a specific event
- `POST /bookings` - Create a new booking
- `GET /users/{id}/bookings` - Get bookings for a specific user

## Technologies Used

- **Backend:** Node.js, Express.js
- **Database:** MySQL with Sequelize ORM
- **Validation:** express-validator
- **Security:** Helmet, CORS
- **Utilities:** UUID for booking codes, dotenv for environment variables

## Project Structure

```
lt_in_assgnmnt/
├── app.js                 # Main application setup
├── server.js              # Server entry point
├── package.json           # Dependencies and scripts
├── Readme.md              # Project documentation
├── documentation/
│   └── ems.yaml          # OpenAPI specification
├── config/
│   └── database.js       # Database configuration
├── controller/
│   ├── eventController.js
│   └── bookingController.js
├── middleware/
│   └── validate.js       # Validation middleware
├── models/
│   ├── index.js
│   ├── event.js
│   ├── user.js
│   ├── booking.js
│   └── event_attendance.js
├── routes/
│   ├── eventRouter.js
│   ├── bookingRouter.js
│   ├── userRouter.js
│   └── eventAttendanceRouter.js
├── utils/
│   └── bookingCodeGenerator.js
└── validators/
    └── validators.js
```

## Live Url
**https://ems-backend-production-a47e.up.railway.app**

