# COVID-19 Bed Slot Booking System

A full-stack web application that lets users search hospitals, check bed availability, and book beds during a health crisis — built with a **FastAPI** backend and a **React + Vite** frontend.

## 🔗 Live Preview
Not deployed yet — run locally:
- Frontend: `http://localhost:5174`
- Backend API: `http://localhost:8000`

## 📸 Preview

**API Documentation (Swagger UI)**
![API Endpoints](Screenshots/Screenshot%202026-07-22%20090035.png)
![API Schemas](Screenshots/Screenshot%202026-07-22%20090050.png)

**Hospital Search & Booking**
![Hospital search results](Screenshots/Screenshot%202026-07-22%20091655.png)
![Hospital search — different city](Screenshots/Screenshot%202026-07-22%20091814.png)
![Hospital search — another city](Screenshots/Screenshot%202026-07-22%20091836.png)

**Login**
![Login page](Screenshots/Screenshot%202026-07-22%20091712.png)

## 🛠️ Built With

**Backend**
- **FastAPI** – REST API framework
- **MySQL** – relational database for hospitals, users, and bookings
- **SQLAlchemy** – ORM for database models
- **Pydantic** – request/response schema validation
- JWT-based authentication (via `auth_utils.py`)

**Frontend**
- **React** – UI library
- **Vite** – build tool and dev server
- **Axios** – API requests to the backend

## ✨ Features
- User signup and login with authentication
- Browse hospitals and view real-time bed availability
- Book a bed slot at a selected hospital
- Dashboard to view and manage bookings
- Hospital data stored and queried from a MySQL database

## 📂 Project Structure
```
Covid-Bed-Booking-System/
│
├── covid-bed-backend/
│   ├── main.py               # FastAPI app entry point
│   ├── database.py           # Database connection setup
│   ├── models.py             # SQLAlchemy models
│   ├── schemas.py            # Pydantic schemas
│   ├── auth_utils.py         # Authentication helpers
│   └── routes/
│       ├── auth.py           # Signup/login routes
│       ├── bookings.py       # Bed booking routes
│       └── hospitals.py      # Hospital listing routes
│
├── covid-bed-frontend/
│   ├── src/
│   │   ├── pages/
│   │   │   ├── Home.jsx
│   │   │   ├── Login.jsx
│   │   │   ├── Signup.jsx
│   │   │   └── Dashboard.jsx
│   │   ├── components/
│   │   │   └── HospitalCard.jsx
│   │   ├── api/
│   │   │   └── axios.js      # Axios instance for API calls
│   │   └── App.jsx
│   └── package.json
│
└── database_of_hospitals.sql # MySQL schema/seed data for hospitals
```

## 🚀 Getting Started

### Prerequisites
- Python 3.9+
- Node.js and npm
- MySQL Server

### Backend Setup
1. Navigate to the backend folder
   ```bash
   cd covid-bed-backend
   ```
2. Install dependencies
   ```bash
   pip install -r requirements.txt
   ```
3. Import the hospital database
   ```bash
   mysql -u your_username -p your_database_name < ../database_of_hospitals.sql
   ```
4. Set up your database connection details in `database.py` (or a `.env` file, if used)
5. Run the FastAPI server
   ```bash
   uvicorn main:app --reload
   ```

### Frontend Setup
1. Navigate to the frontend folder
   ```bash
   cd covid-bed-frontend
   ```
2. Install dependencies
   ```bash
   npm install
   ```
3. Run the development server
   ```bash
   npm run dev
   ```

The frontend will typically run on `http://localhost:5173` and the backend on `http://localhost:8000`.

## 📌 Notes
This project is for **educational purposes only**, built to practice full-stack development — combining a Python/FastAPI backend with a React frontend and MySQL database.

## 👤 Author
**Nilanshu Tiwary**
GitHub: [@definetlyNot22](https://github.com/definetlyNot22)

## 📄 License
This project is open source and available for learning purposes.
