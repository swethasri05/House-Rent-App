
# House Rental App - MERN Stack Project

This is a full-stack house rental application built using the **MERN stack** (MongoDB, Express.js, React, Node.js). This README file outlines the setup instructions and API usage for the user registration feature.

## Table of Contents
- [Prerequisites](#prerequisites)
- [Getting Started](#getting-started)
- [Project Structure](#project-structure)
- [API Endpoints](#api-endpoints)
- [Environment Variables](#environment-variables)
- [Technologies Used](#technologies-used)
- [License](#license)

---

## Prerequisites

Make sure you have the following installed:
- [Node.js](https://nodejs.org/) (v14+ recommended)
- [MongoDB](https://www.mongodb.com/) (local or cloud instance)
- [Git](https://git-scm.com/) (optional)

## Getting Started

1. **Clone the repository**

   ```bash
   git clone https://github.com/your-username/house-rental-app.git
   cd house-rental-app
   ```

2. **Install dependencies**

   Navigate to the root folder and install server dependencies:

   ```bash
   npm install
   ```

3. **Set up environment variables**

   Create a `.env` file in the root directory and add the following variables:

   ```plaintext
   MONGO_URI=<your_mongodb_connection_string>
   PORT=3000
   ```

4. **Run the server**

   Start the backend server:

   ```bash
   npm start
   ```

   The server will start on `http://localhost:3000` by default.

---

## Project Structure

Here's a quick overview of the project's file structure:

```plaintext
.
├── controllers/
│   └── userController.js       # User registration and login logic
├── models/
│   └── userModel.js            # Mongoose schema for the User model
├── routes/
│   └── userRoutes.js           # Routes for user-related operations
├── .env                        # Environment variables
├── app.js                      # Main server file
└── README.md                   # Project documentation
```

## API Endpoints

### User Registration

**Endpoint:** `/api/users/register`  
**Method:** `POST`  
**Description:** Registers a new user in the database.

#### Request Body

| Field     | Type   | Required | Description           |
| --------- | ------ | -------- | --------------------- |
| `name`    | String | Yes      | User's full name      |
| `email`   | String | Yes      | User's email address  |
| `password`| String | Yes      | User's password       |
| `type`    | String | Yes      | User's type (e.g., tenant, landlord) |

#### Sample Request

```json
{
  "name": "John",
  "email": "john.doe@example.com",
  "password": "password123",
  "type": "tenant"
}
```

#### Sample Response

```json
{
  "message": "User registered successfully"
}
```

---

## Environment Variables

- `MONGO_URI`: MongoDB connection string for connecting to your database.
- `PORT`: Port for the backend server (default is 3000).

## Technologies Used

- **Backend**: Node.js, Express.js, MongoDB, Mongoose
- **Other Libraries**: bcrypt (for password hashing), dotenv (for environment variable management)

---

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more information.
```

### Explanation of README Sections
- **Prerequisites**: Lists software needed to run the project.
- **Getting Started**: Explains steps to set up and start the project.
- **Project Structure**: Shows key project files and folders.
- **API Endpoints**: Details the registration API with example JSON request/response.
- **Environment Variables**: Defines necessary environment variables and their purposes.
- **Technologies Used**: Highlights main technologies and libraries.
- **License**: Specifies project licensing information.

This README should provide all the necessary details to help new developers or contributors get started with your project!
