# ⚓ EDUMARINE

A comprehensive full-stack web application designed for educational and marine-related management. The platform provides dedicated panels and dashboards for distinct user roles, including Students, Vendors, and Administrators, facilitating seamless course and user management.

## 🚀 Features

* **Role-Based Dashboards:** Dedicated panels for Students and Vendors with tailored functionalities.
* **Course Management:** View, manage, and enroll in available courses.
* **Secure Authentication:** Integrated user authentication and authorization (`AuthContext`, JWT middleware).
* **Modern User Interface:** Built with React and styled using Tailwind CSS for a fully responsive experience.
* **Robust Backend API:** RESTful architecture built with Node.js and Express, handling modular routes for courses, students, and vendors.
* **Containerized:** Includes a `docker-compose.yml` for simplified setup and scalable deployment.

## 🛠️ Tech Stack

**Frontend (`/client`)**
* **Framework:** React.js
* **Styling:** Tailwind CSS
* **State Management:** React Context API (`AuthContext`)
* **Routing:** React Router (`routes.js`)

**Backend (`/server`)**
* **Environment:** Node.js
* **Framework:** Express.js (Inferred)
* **Architecture:** MVC Pattern (Models, Views/Routes, Controllers)
* **Authentication:** Custom Auth Middleware

**DevOps & Tools**
* Docker & Docker Compose
* Bash Scripting (`deploy.sh`)

## 📂 Project Structure

```text
EDUMARINE/
│
├── client/                     # Frontend Application
│   ├── public/                 # Static assets
│   ├── src/
│   │   ├── components/         # Reusable UI (Navbar, CourseList, Dashboards)
│   │   ├── context/            # Global state (AuthContext)
│   │   ├── hooks/              # Custom React hooks (useAuth)
│   │   ├── pages/              # Main application views (Home, Courses, Profile)
│   │   ├── services/           # API integration (api.js)
│   │   └── styles/             # Global styles and theming
│   ├── tailwind.config.js      # Tailwind CSS configuration
│   └── package.json            # Frontend dependencies
│
├── server/                     # Backend Application
│   ├── src/
│   │   ├── config/             # Database and environment configurations
│   │   ├── controllers/        # Request handling logic
│   │   ├── middleware/         # Custom middlewares (auth, error handling)
│   │   ├── models/             # Database schemas (Course, Student, User, Vendor)
│   │   └── routes/             # API endpoint definitions
│   ├── server.js               # Backend entry point
│   ├── .env                    # Environment variables
│   └── package.json            # Backend dependencies
│
├── docs/                       # Project documentation
├── scripts/                    # Deployment scripts (deploy.sh)
└── docker-compose.yml          # Docker orchestration file
⚙️ Getting Started
Follow these steps to set up the project on your local machine.

Prerequisites
Node.js (v16 or higher recommended)

npm or yarn

Docker (optional, for containerized environments)

💻 Local Setup
1. Clone the repository:

Bash
git clone [https://github.com/mansiym13-sketch/EDUMARINE.git](https://github.com/mansiym13-sketch/EDUMARINE.git)
cd EDUMARINE
2. Setup the Backend:
Open a new terminal window, navigate to the server directory, and install dependencies:

Bash
cd server
npm install
Note: Make sure to configure your .env file in the server directory with your database URI and JWT secrets before starting.

Bash
npm start # or npm run dev
3. Setup the Frontend:
Open another terminal window, navigate to the client directory, and install dependencies:

Bash
cd client
npm install
Start the React development server:

Bash
npm start
The frontend should now be running (typically on http://localhost:3000).

🐳 Docker Setup
If you prefer to run the entire stack using Docker, simply run the following command from the root directory:

Bash
docker-compose up --build
This will containerize both the client and server applications and spin them up together.
