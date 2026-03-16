# MediBook - Smart Medical Appointment System

A full-stack MERN application for managing medical appointments with role-based access control for Patients, Doctors, and Admins.

![MERN Stack](https://img.shields.io/badge/Stack-MERN-green)
![License](https://img.shields.io/badge/License-MIT-blue)

## 🚀 Features

### For Patients
- 👤 Self-registration and login
- 🔍 Browse available doctors with specializations
- 📅 Book appointments with preferred doctors
- 📊 View appointment history and status
- ❌ Cancel pending appointments

### For Doctors
- 📋 View all appointment requests
- ✅ Accept or reject appointments
- 📆 Manage confirmed appointments
- 👨‍⚕️ Update profile and availability

### For Admins
- ➕ Add new doctors to the system
- 📈 View system analytics (total doctors, patients, appointments)
- 👥 Manage platform users

## 🛠️ Tech Stack

**Frontend:**
- React.js (Vite)
- Tailwind CSS
- React Router DOM
- Axios

**Backend:**
- Node.js
- Express.js
- MongoDB (Mongoose)
- JWT Authentication
- bcrypt.js

## 📋 Prerequisites

- Node.js (v14 or higher)
- MongoDB (running locally or MongoDB Atlas)
- npm or yarn

## ⚙️ Installation

### 1. Clone the repository
```bash
git clone https://github.com/yourusername/medibook.git
cd medibook
```

### 2. Backend Setup
```bash
cd server
npm install
```

Create a `.env` file in the `server` directory:
```env
PORT=5000
MONGO_URI=mongodb://127.0.0.1:27017/medical_appointment_system
JWT_SECRET=your_secure_jwt_secret_key_here
```

### 3. Frontend Setup
```bash
cd client
npm install
```

### 4. Seed Database (Optional)
```bash
cd server
node seed.js
```

This creates default accounts:
- **Admin**: `admin@example.com` / `admin123`
- **Doctor**: `doctor@example.com` / `doctor123`
- **Patient**: `patient@example.com` / `patient123`

## 🚀 Running the Application

### Start Backend Server
```bash
cd server
npm run dev
```
Server runs on `http://localhost:5000`

### Start Frontend
```bash
cd client
npm run dev
```
Client runs on `http://localhost:5173`

## 📁 Project Structure

```
medibook/
├── client/                 # React frontend
│   ├── src/
│   │   ├── components/    # Reusable components
│   │   ├── pages/         # Page components
│   │   ├── context/       # Auth context
│   │   ├── api.js         # Axios configuration
│   │   └── App.jsx        # Main app component
│   └── package.json
│
├── server/                # Express backend
│   ├── models/           # Mongoose schemas
│   ├── controllers/      # Route controllers
│   ├── routes/           # API routes
│   ├── middleware/       # Auth middleware
│   ├── seed.js           # Database seeder
│   └── index.js          # Server entry point
│
└── README.md
```

## 🔐 API Endpoints

### Authentication
- `POST /api/auth/register` - Register new patient
- `POST /api/auth/login` - Login (all roles)
- `GET /api/auth/user` - Get current user

### Doctors
- `GET /api/doctors` - Get all doctors
- `POST /api/doctors` - Add doctor (Admin only)
- `PUT /api/doctors/profile` - Update doctor profile

### Appointments
- `POST /api/appointments/book` - Book appointment (Patient)
- `GET /api/appointments/my-appointments` - Get patient appointments
- `GET /api/appointments/doctor-appointments` - Get doctor appointments
- `PUT /api/appointments/status/:id` - Update appointment status (Doctor)

### Admin
- `GET /api/admin/stats` - Get system statistics

## 🎨 UI Features

- Modern gradient backgrounds
- Responsive design for all devices
- Interactive hover effects
- Smooth transitions and animations
- Role-based tabbed login interface
- Real-time status badges
- Modal dialogs for booking

## 🔒 Security Features

- JWT token-based authentication
- Password hashing with bcrypt
- Protected routes with middleware
- Role-based access control
- Secure HTTP-only practices

## 📝 License

This project is licensed under the MIT License.

## 👨‍💻 Author

Shubham Kumar Sinha - [GitHub](https://github.com/Shubham-kr-sinha)

## 🤝 Contributing

Contributions, issues, and feature requests are welcome!
