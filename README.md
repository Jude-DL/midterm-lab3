# MERN Stack CRUD Application

A full-stack web application built with MongoDB, Express.js, React, and Node.js that demonstrates CRUD (Create, Read, Update, Delete) operations.

## Features

- ✅ Create new users
- ✅ Read/Display all users
- ✅ Update existing users
- ✅ Delete users
- ✅ Responsive UI design
- ✅ Real-time data updates
- ✅ Form validation
- ✅ Error handling

## Technologies Used

### Backend
- **Node.js** - Runtime environment
- **Express.js** - Web framework
- **MongoDB** - NoSQL database
- **Mongoose** - MongoDB object modeling
- **CORS** - Cross-origin resource sharing
- **dotenv** - Environment variables

### Frontend
- **React** - Frontend library
- **Axios** - HTTP client for API requests
- **CSS3** - Styling and responsive design

## Project Structure

```
midterm_lab_3/
├── frontend/                 # React application
│   ├── src/
│   │   ├── App.js           # Main React component
│   │   ├── App.css          # Styling
│   │   └── ...
│   └── package.json
├── models/
│   └── User.js              # User data model
├── routes/
│   └── userRoutes.js        # API routes for CRUD operations
├── server.js                # Express server setup
├── package.json             # Backend dependencies
└── .env                     # Environment variables
```

## Prerequisites

Before running this application, make sure you have the following installed:
- **Node.js** (v14 or higher)
- **MongoDB** (local installation or MongoDB Atlas)
- **npm** or **yarn**

## Installation & Setup

### 1. Clone and Install Dependencies

```bash
# Install backend dependencies
npm install

# Install frontend dependencies
cd frontend
npm install
cd ..
```

### 2. MongoDB Setup

**Option A: Local MongoDB**
- Install MongoDB locally
- Make sure MongoDB service is running
- The application will connect to `mongodb://localhost:27017/mern_crud_app`

**Option B: MongoDB Atlas (Cloud)**
- Create a free account at [MongoDB Atlas](https://www.mongodb.com/atlas)
- Create a new cluster
- Get your connection string
- Update the `.env` file with your MongoDB Atlas connection string

### 3. Environment Configuration

Update the `.env` file with your MongoDB connection:

```env
MONGODB_URI=mongodb://localhost:27017/mern_crud_app
PORT=5000
```

## Running the Application

### Development Mode (Both Frontend and Backend)

```bash
# Run both frontend and backend concurrently
npm run dev
```

### Run Backend Only

```bash
# Start the Express server
npm run server
```

### Run Frontend Only

```bash
# Start the React development server
npm run client
```

## API Endpoints

The backend provides the following REST API endpoints:

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/api/users` | Get all users |
| GET | `/api/users/:id` | Get user by ID |
| POST | `/api/users` | Create new user |
| PUT | `/api/users/:id` | Update user by ID |
| DELETE | `/api/users/:id` | Delete user by ID |

### Example API Usage

**Create User:**
```bash
POST http://localhost:5000/api/users
Content-Type: application/json

{
  "name": "John Doe",
  "email": "john@example.com",
  "age": 25,
  "occupation": "Software Developer"
}
```

## User Interface

The React frontend provides:

1. **Add User Form** - Input fields for name, email, age, and occupation
2. **Users List** - Grid display of all users with their information
3. **Edit Functionality** - Click "Edit" to modify user data
4. **Delete Functionality** - Click "Delete" to remove users (with confirmation)
5. **Real-time Updates** - UI updates immediately after CRUD operations

## How to Use

1. **Start the application** using `npm run dev`
2. **Open your browser** and go to `http://localhost:3000`
3. **Add users** by filling out the form and clicking "Add User"
4. **View users** in the users grid below the form
5. **Edit users** by clicking the "Edit" button on any user card
6. **Delete users** by clicking the "Delete" button (with confirmation)

## Learning Objectives Achieved

✅ **Understanding MERN stack structure and workflow**
- Complete separation of frontend (React) and backend (Express/MongoDB)
- RESTful API design and implementation

✅ **Building RESTful API with Express.js and MongoDB**
- Express server setup with middleware
- MongoDB connection using Mongoose
- API endpoints for all CRUD operations

✅ **CRUD operations implementation**
- Create: Add new users via POST request
- Read: Display users via GET request
- Update: Edit users via PUT request
- Delete: Remove users via DELETE request

✅ **React frontend connected to Node.js/Express backend**
- Component-based React architecture
- State management with React hooks
- Form handling and validation

✅ **Axios implementation for API requests**
- HTTP client setup and configuration
- Error handling and loading states
- Real-time data synchronization

## Troubleshooting

**Common Issues:**

1. **MongoDB Connection Error**
   - Ensure MongoDB is running locally or check Atlas connection string
   - Verify network access and firewall settings

2. **CORS Errors**
   - Make sure CORS is properly configured in server.js
   - Check that frontend is running on http://localhost:3000

3. **Port Already in Use**
   - Change the PORT in .env file
   - Kill existing processes using the ports

4. **Dependencies Not Found**
   - Run `npm install` in both root and frontend directories
   - Clear npm cache: `npm cache clean --force`

## Next Steps

To extend this application, consider adding:
- User authentication and authorization
- Input validation and sanitization
- Pagination for large datasets
- Search and filter functionality
- Image uploads
- Unit and integration tests
- Docker containerization
- Deployment to cloud platforms

## Contributing

Feel free to fork this project and submit pull requests for any improvements!