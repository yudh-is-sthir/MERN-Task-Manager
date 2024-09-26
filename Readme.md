# MERN Task Manager

This is a full-stack MERN (MongoDB, Express, React, Node.js) application for managing tasks. It includes a backend server using Express and MongoDB, and a frontend client using React and Redux.

## Prerequisites

Before running the application, ensure you have the following installed:

- [Node.js](https://nodejs.org/)
- [pnpm](https://pnpm.io/installation) (as the package manager)
- [MongoDB](https://www.mongodb.com/try/download/community) (running locally or a remote instance)

## Installation

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/mern-task-manager.git
cd mern-task-manager
```

### 2. Install Dependencies

You need to install dependencies for both the frontend and backend. Use `pnpm` for package installation.

```bash
pnpm install-all
```

This script installs all dependencies for both the frontend and backend.

### 3. Setup Environment Variables

Create a `.env` file in the `backend` directory with the following configuration:

```plaintext
PORT=5000
MONGO_URI=mongodb://localhost:27017/tasks  # Update with your MongoDB URI
JWT_SECRET=your_jwt_secret                 # Replace with your secret key
```

Make sure to replace `MONGO_URI` with your actual MongoDB connection string and `JWT_SECRET` with a strong secret key.

## Running the Application

### 1. Start MongoDB

Ensure MongoDB is running. You can start MongoDB using:

```bash
mongod
```

or if using MongoDB as a service:

```bash
sudo service mongod start
```

### 2. Run the Application

To start both the frontend and backend servers concurrently, run:

```bash
pnpm run dev
```

This will start the backend on port `5000` and the frontend on port `3000`. The app will automatically open in your default browser at `http://localhost:3000`.

### 3. Backend Endpoints

The backend API is accessible at `http://localhost:5000/api`. Below are some key routes:

- `POST /api/auth/register`: Register a new user
- `POST /api/auth/login`: Login user
- `GET /api/tasks`: Get all tasks (requires authentication)
- `POST /api/tasks`: Create a new task (requires authentication)
- `PUT /api/tasks/:id`: Update a task (requires authentication)
- `DELETE /api/tasks/:id`: Delete a task (requires authentication)

## Available Scripts

In the project root directory, you can run the following scripts:

- `pnpm run dev`: Start both frontend and backend concurrently
- `pnpm run dev-client`: Start only the frontend (React)
- `pnpm run dev-server`: Start only the backend (Express)
- `pnpm run build`: Build the frontend for production

## Technologies Used

- **Frontend**: React, Redux, React Router, Axios, TailwindCSS
- **Backend**: Node.js, Express, Mongoose, JSON Web Token (JWT), bcrypt
- **Database**: MongoDB

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.

---

Let me know if you need any modifications!