# Community Problem Solver

A modern full-stack platform for citizens, volunteers, and administrators to report, discuss, track, and resolve local community issues.

---

## 🚀 Project Overview

Community Problem Solver is designed to help neighborhoods and local governments collaborate on real-world issues such as streetlight outages, waste collection, road repairs, and volunteer coordination.
It combines a React + Vite front end with an Express + MongoDB back end, delivering an experience that supports problem reporting, solution voting, discussion threads, notifications, volunteer management, and analytics.

## ✨ Key Features

- **User registration & authentication** with JWT-based protected APIs.
- **Problem submission** with descriptions, status tracking, and location details.
- **Solution proposals** and **voting system** to promote the best community responses.
- **Discussion threads** on each problem for collaboration and feedback.
- **Volunteer applications** with region-specific dashboards.
- **Admin dashboard** for user management, analytics, problem moderation, and approvals.
- **Notifications** for user actions such as votes, discussions, and status updates.
- **Image upload support** via Cloudinary.
- **AI suggestions** endpoint for enhancing problem-solving workflows.
- **Seed data script** to bootstrap demo users, volunteers, problems, solutions, and notifications.

## 🧩 Tech Stack

- Frontend: `React`, `Vite`, `Tailwind CSS`, `Axios`, `React Router`
- Backend: `Node.js`, `Express`, `MongoDB`, `Mongoose`
- Authentication: `jsonwebtoken`, password hashing with `bcrypt`
- File upload: `multer`, `cloudinary`
- Notifications: `nodemailer`

## 📂 Repository Structure

```
/ client/    # React front-end application
/ server/    # Express back-end API server
```

## ⚙️ Setup Instructions

### 1. Backend

```powershell
cd server
npm install
```

Create a `.env` file in `server/` with the following variables:

```env
MONGODB_URL=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret
CLOUD_NAME=your_cloudinary_cloud_name
API_KEY=your_cloudinary_api_key
API_SECRET=your_cloudinary_api_secret
SMTP_HOST=your_smtp_host
SMTP_PORT=your_smtp_port
SMTP_USER=your_smtp_username
SMTP_PASS=your_smtp_password
FROM_EMAIL=your_email_address
FRONTEND_URL=http://localhost:5173
CORS_ORIGINS=http://localhost:5173,http://localhost:3000
PORT=3000
```

Start the backend server:

```powershell
npm run dev
```

### 2. Frontend

```powershell
cd client
npm install
npm run dev
```

The app runs by default at `http://localhost:5173`.

## 🧪 Seed Data & Demo Accounts

A seed script is available to create mock users, volunteers, problems, solutions, discussions, and notifications.

```powershell
cd server
node scripts/seedMockData.js
```

### Example seeded accounts

- Admin: `mohan62131@gmail.com` / `mohan@62131`
- Demo user: `charan.mock@cps.local` / `123456`
- Volunteers: one account per state, e.g. `delhi.volunteer@cps.local` / `Delhi@123`

## 📌 Available Scripts

### Backend

- `npm start` — run server normally
- `npm run dev` — run server with `nodemon`

### Frontend

- `npm run dev` — start Vite development server
- `npm run build` — build production assets
- `npm run preview` — preview built frontend

## 💡 Notes

- The backend API is mounted under `/api/*` and the app expects authenticated requests for most operations.
- The seed script is a great way to verify the app flows without manually creating data.
- Update `.env` values before running the application in a production environment.

---

## 📞 Contact

If you want to improve the README further, I can add screenshots, architecture diagrams, or a step-by-step demo flow next.
