# Task Management System

A comprehensive full-stack web application for managing tasks and teams with role-based access control, built with React and Node.js.

## 🌟 Features

### Admin Features

- **Dashboard Analytics**: Visual insights with charts and statistics
- **Task Management**: Create, update, delete, and assign tasks
- **User Management**: Manage team members and their roles
- **Reporting**: Generate Excel reports for tasks and analytics

### User Features

- **Personal Dashboard**: Overview of assigned tasks and progress
- **My Tasks**: View and manage assigned tasks
- **Task Details**: Detailed view of task information with attachments
- **Profile Management**: Update profile and avatar

### Common Features

- **Authentication**: Secure login/signup with JWT tokens
- **File Uploads**: Support for task attachments and profile images
- **Real-time Updates**: Dynamic status updates and notifications
- **Responsive Design**: Works seamlessly on desktop and mobile
- **Role-based Access**: Admin and member role distinctions

## 🛠️ Tech Stack

### Frontend

- **React 19** - Modern UI library
- **Vite** - Fast build tool and development server
- **Tailwind CSS** - Utility-first CSS framework
- **React Router DOM** - Client-side routing
- **Axios** - HTTP client for API calls
- **Recharts** - Data visualization charts
- **React Hot Toast** - Notification system
- **React Icons** - Icon library
- **Moment.js** - Date manipulation

### Backend

- **Node.js** - JavaScript runtime
- **Express.js** - Web application framework
- **MongoDB** - NoSQL database
- **Mongoose** - MongoDB object modeling
- **JWT** - JSON Web Token authentication
- **Bcrypt.js** - Password hashing
- **Multer** - File upload handling
- **ExcelJS** - Excel file generation
- **CORS** - Cross-origin resource sharing

## 📁 Project Structure

```
TaskManagementSystem/
├── client/                 # Frontend React application
│   ├── src/
│   │   ├── components/     # Reusable UI components
│   │   │   ├── Cards/      # Card components
│   │   │   ├── Charts/     # Chart components
│   │   │   ├── Inputs/     # Form input components
│   │   │   └── layouts/    # Layout components
│   │   ├── context/        # React context providers
│   │   ├── hooks/          # Custom React hooks
│   │   ├── pages/          # Page components
│   │   │   ├── Admin/      # Admin-specific pages
│   │   │   ├── Auth/       # Authentication pages
│   │   │   └── User/       # User-specific pages
│   │   ├── routes/         # Route protection
│   │   └── utils/          # Utility functions
│   └── public/             # Static assets
└── server/                 # Backend Node.js application
    ├── config/             # Database configuration
    ├── controllers/        # Request handlers
    ├── middlewares/        # Custom middleware
    ├── models/             # Database models
    ├── routes/             # API route definitions
    └── uploads/            # File upload storage
```

## 🚀 Getting Started

### Prerequisites

- Node.js (v18 or higher)
- MongoDB (local or cloud instance)
- npm or yarn package manager

### Installation

1. **Clone the repository**

   ```bash
   git clone https://github.com/AmulyaJain2004/TaskManagementSystem.git
   cd TaskManagementSystem
   ```

2. **Install Backend Dependencies**

   ```bash
   cd server
   npm install
   ```

3. **Install Frontend Dependencies**

   ```bash
   cd ../client
   npm install
   ```

4. **Environment Setup**

   Create a `.env` file in the `server` directory:

   ```env
   MONGODB_URI=mongodb://localhost:27017/taskmanagement
   JWT_SECRET=your_jwt_secret_key
   PORT=5000
   ```

5. **Start the Development Servers**

   **Backend** (from server directory):

   ```bash
   npm run dev
   ```

   **Frontend** (from client directory):

   ```bash
   npm run dev
   ```

6. **Access the Application**
   - Frontend: `http://localhost:5173`
   - Backend API: `http://localhost:5000`

## 📋 API Endpoints

### Authentication

- `POST /api/auth/register` - User registration
- `POST /api/auth/login` - User login

### Users

- `GET /api/users` - Get all users (Admin only)
- `GET /api/users/profile` - Get user profile
- `PUT /api/users/profile` - Update user profile

### Tasks

- `GET /api/tasks` - Get all tasks
- `POST /api/tasks` - Create new task (Admin only)
- `PUT /api/tasks/:id` - Update task
- `DELETE /api/tasks/:id` - Delete task (Admin only)
- `GET /api/tasks/user/:userId` - Get user-specific tasks

### Reports

- `GET /api/reports/excel` - Generate Excel report (Admin only)

## 🔐 Authentication & Authorization

The application implements JWT-based authentication with role-based access control:

- **Public Routes**: Login, Signup
- **Protected Routes**: All dashboard and task-related pages
- **Admin-only Features**: User management, task creation/deletion, reports
- **User Features**: View assigned tasks, update task status

## 🎨 UI/UX Features

- **Modern Design**: Clean and intuitive interface with Tailwind CSS
- **Responsive Layout**: Optimized for desktop and mobile devices
- **Interactive Charts**: Visual analytics using Recharts
- **File Upload**: Drag-and-drop file upload with preview
- **Progress Indicators**: Visual task progress tracking
- **Toast Notifications**: Real-time feedback for user actions

## 🔧 Configuration

### Database Models

**User Model:**

- Name, email, password
- Profile image URL
- Role (admin/member)
- Timestamps

**Task Model:**

- Title, description, priority
- Status (Pending/In Progress/Completed)
- Due date, assigned users
- Attachments, todo items
- Creator and timestamps

## 🚀 Deployment

### Frontend (Vercel)

The frontend is configured for Vercel deployment with proper CORS settings.

### Backend

Set up environment variables and deploy to your preferred platform (Heroku, Railway, etc.).

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 👥 Author

**Amulya Jain** - [GitHub](https://github.com/AmulyaJain2004)

## 📞 Support

For support, create an issue in the GitHub repository.

---

Built with ❤️ using React and Node.js
