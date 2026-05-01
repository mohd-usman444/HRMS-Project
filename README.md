# HRMS - Human Resource Management System

A full-stack Human Resource Management System (HRMS) built with the MERN stack (MongoDB, Express, React, Node.js). This system features separate dashboards for Administrators and Employees, with role-based access control, attendance tracking, and leave management.

## 🚀 Features

### For Administrators
- **Employee Management**: View, add, and remove employee records.
- **Leave Management**: Review, approve, or reject employee leave requests.
- **Attendance Reports**: View and filter attendance records across the organization.
- **Dashboard**: High-level overview of employee data.

### For Employees
- **Personal Profile**: View and manage personal information.
- **Attendance Tracking**: Mark daily attendance with a single click.
- **Leave Requests**: Apply for various types of leave (Casual, Sick, Annual, etc.) and track their status.
- **Notifications**: Receive in-app and email notifications when leave requests are processed.

## 🛠️ Tech Stack

- **Frontend**: React.js, Vite, Tailwind CSS (or Vanilla CSS), Lucide React (icons), React Hot Toast.
- **Backend**: Node.js, Express.js.
- **Database**: MongoDB (Mongoose).
- **Authentication**: JSON Web Token (JWT) with separate sessions for Admin and Employees.
- **Emails**: Nodemailer.

## 📦 Installation & Setup

1. **Clone the repository**:
   ```bash
   git clone https://github.com/mohd-usman444/HRMS-Project.git
   cd HRMS-Project
   ```

2. **Install Dependencies**:
   ```bash
   # Install server dependencies
   cd server
   npm install

   # Install client dependencies
   cd ../client
   npm install
   ```

3. **Environment Variables**:
   Create a `.env` file in the `server` directory and add:
   ```env
   PORT=5000
   MONGO_URI=your_mongodb_uri
   JWT_SECRET=your_secret_key
   ADMIN_SECRET_KEY=your_admin_key
   
   # For Email Notifications
   EMAIL_HOST=smtp.gmail.com
   EMAIL_PORT=465
   EMAIL_USER=your_email@gmail.com
   EMAIL_PASS=your_app_password
   EMAIL_FROM=your_email@gmail.com
   ```

4. **Run the Application**:
   ```bash
   # Start the backend (from server folder)
   npm run dev

   # Start the frontend (from client folder)
   npm run dev
   ```

## 🔒 Security Features
- **Session Separation**: Admin and Employee sessions are stored independently, allowing both to be open simultaneously in the same browser without interference.
- **Protected Routes**: Middleware ensures that users can only access pages allowed by their specific role.

---
Created by [Mohd Usman](https://github.com/mohd-usman444)
