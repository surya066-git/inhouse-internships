🎓 Inhouse Internships 2.0
Node.js Version React Version Vite Version License

A high-performance, responsive Internship Management System tailored for universities. It provides a unified, secure portal for Students, Faculty, HODs, and Administrators to track, review, and approve inhouse internships.

🚀 Key Features
👥 Role-Based Portals & Dashboards
Students: Submit daily status logs, submit weekly tasks, check review ratings, and track attendance.
Faculty Mentors: Monitor daily logs, review and grade weekly task submissions, record attendance, and submit project reviews.
HODs (Heads of Department): View department-wide statistics, assign projects and mentors, and track student outcomes.
Administrators: Complete system configuration, user importing/exporting (via Excel), mail template tuning, system audits, and batch-wise settings.
🛡️ Core Security & System Audits
Robust JWT Auth: Stateless token authorization enhanced with token versioning for instant logouts.
Secure OTP Flow: Automatic email OTP verification for secure registrations and password resets.
Login Audits: Instant logging of all successful and failed authentication attempts, tracking timestamps and IP addresses.
Strict Validations: Input sanitization and Schema validations on all API endpoints.
📂 Project Architecture
The workspace is split into two primary components:

📂 frontend/: A React 19 app powered by Vite and Material-UI (MUI). Uses role-based private routing, notistack, and an elegant dark theme.
📂 backend/: A RESTful Node.js/Express microservice configured with Mongoose (MongoDB), Nodemailer, and JWT helpers.
🛠️ Technology Stack
Frontend	Backend	DevOps & Utilities
React 19 & React Router 7	Node.js & Express	ESLint & Prettier
Vite 7	MongoDB & Mongoose	Docker & Docker Compose
Material-UI (MUI)	Nodemailer (SMTP)	Git & GitHub Actions
Axios & Notistack	JWT & bcryptjs	Jenkinsfile
🏁 Getting Started
Prerequisites
Node.js (v18.0.0 or higher)
MongoDB (Local server or Atlas cloud cluster)
Git
Installation & Local Setup
Clone the repository:

git clone https://github.com/tnscharan/Inhouse-Internships.git
cd Inhouse-Internships
Configure Backend:

cd backend
npm install
cp .env.example .env
# Update MONGO_URI, JWT_SECRET, and SMTP configurations inside .env
Configure Frontend:

cd ../frontend
npm install
cp .env.example .env
# Set VITE_API_TARGET to your local backend server URL (default: http://localhost:5000)
Running Locally
To run both backend and frontend servers concurrently:

# In the project root directory
npm start
Alternatively, launch them individually:

Backend: cd backend && npm run dev
Frontend: cd frontend && npm run dev
🐳 Docker Deployment
To launch the complete application stack (Frontend, Backend, and MongoDB) inside containers:

docker-compose up --build
This maps the frontend client to port 80 (or 3000 depending on configuration) and the API server to port 5000.

📄 License
Distributed under the MIT License. See LICENSE for more information.
