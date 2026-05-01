# 👔 HRMS - Human Resource Management System

[![MERN Stack](https://img.shields.io/badge/Stack-MERN-blue.svg)](https://mongodb.com)
[![React](https://img.shields.io/badge/Frontend-React-61DAFB.svg)](https://reactjs.org)
[![Node.js](https://img.shields.io/badge/Backend-Node.js-339933.svg)](https://nodejs.org)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

A sophisticated, full-stack Human Resource Management System designed to streamline organizational workflows. This project demonstrates high-level implementation of **Role-Based Access Control (RBAC)**, real-time data synchronization, and a seamless multi-user experience.

---

## 🌟 Project Impact

This isn't just a basic CRUD app. It is a robust enterprise-ready solution that addresses real-world HR challenges:

- **Dual-Session Integrity**: Solved the common "Session Overwrite" problem. Admin and Employees can operate simultaneously in different tabs without cross-authentication issues.
- **Automated Communication**: Integrated email and in-app notification systems to ensure transparency in leave management.
- **Data-Driven Insights**: Comprehensive reporting tools for attendance and leave cycles.

---

## 📸 Dashboard Preview

> **Note**: Add your stunning screenshots here to wow your visitors!

---

## 🚀 Core Functionalities

### 🛡️ Administrative Power
- **Full Employee Lifecycle**: Manage staff from onboarding (Add) to offboarding (Remove).
- **Intelligent Leave Processing**: A dedicated workspace to approve or reject requests with automated feedback loops.
- **Advanced Attendance Analytics**: Searchable and filterable data to track punctuality and trends.

### 👤 Employee Experience
- **Interactive Dashboard**: Real-time summary of personal profile and records.
- **One-Click Attendance**: Efficient check-in system with duplicate prevention logic.
- **Transparency**: Detailed leave history with status tracking and instant notifications.

---

## 🛠️ Technical Architecture

```mermaid
graph TD
    A[Client - React] -->|JWT Auth| B[API Gateway - Express]
    B -->|Middleware| C[Role Check]
    C -->|Controllers| D[Logic Layer]
    D -->|Mongoose| E[Database - MongoDB]
    D -->|Nodemailer| F[Email Service]
```

- **Frontend**: Optimized with **Vite** for blazing-fast performance.
- **State Management**: Built-in React Context API for lightweight, efficient state handling.
- **Security**: 
  - JWT (JSON Web Tokens) for secure, stateless authentication.
  - Bcrypt for high-security password hashing.
  - Helmet & CORS for backend protection.

---

## 📡 API Reference

### Authentication
- `POST /api/auth/admin/signup` - Register a new admin
- `POST /api/auth/admin/signin` - Admin login
- `POST /api/auth/user/signup` - Employee registration
- `POST /api/auth/user/signin` - Employee login

### Employee Management (Admin)
- `GET /api/admin/employees` - Get all employees
- `POST /api/admin/employees` - Add a new employee
- `GET /api/admin/employees/:id` - Get single employee details
- `DELETE /api/admin/employees/:id` - Remove an employee

### Attendance
- `POST /api/attendance/mark` - Mark today's attendance (Employee)
- `GET /api/attendance/my` - Get own attendance history (Employee)
- `GET /api/attendance/all` - View all attendance records (Admin)

### Leave Management
- `POST /api/leave/apply` - Submit a leave request (Employee)
- `GET /api/leave/my` - View own leave requests (Employee)
- `GET /api/leave/all` - View all pending requests (Admin)
- `PUT /api/leave/:id/status` - Approve or Reject leave (Admin)

### Notifications
- `GET /api/notifications` - Fetch user-specific notifications
- `PUT /api/notifications/:id/read` - Mark a notification as read
- `PUT /api/notifications/read-all` - Mark all notifications as read

---

## ⚙️ Quick Start

### Prerequisites
- Node.js (v14+)
- MongoDB (Local or Atlas)

### Setup
1. **Clone & Install**:
   ```bash
   git clone https://github.com/mohd-usman444/HRMS-Project.git
   cd HRMS-Project
   cd server && npm install
   cd ../client && npm install
   ```

2. **Environment Variables**:
   Configure your `server/.env` with your Mongo URI and SMTP credentials to enable the notification engine.

3. **Launch**:
   ```bash
   # Terminal 1 (Server)
   npm run dev
   # Terminal 2 (Client)
   npm run dev
   ```

---

## 🗺️ Roadmap
- [ ] Shift Tracking & Scheduling
- [ ] Payroll Integration
- [ ] Performance Review Module
- [ ] Export Reports to PDF/Excel

---

## 🤝 Contributing
Contributions, issues, and feature requests are welcome! Feel free to check the [issues page](https://github.com/mohd-usman444/HRMS-Project/issues).

---

**Show your support by giving a ⭐️ if this project inspired you!**

Created with ❤️ by [Mohd Usman](https://github.com/mohd-usman444)
