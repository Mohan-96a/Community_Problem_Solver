# Community Problem Solver

A modern full-stack platform that helps residents, volunteers, and local administrators report, discuss, track, and resolve community issues.

---

## Overview

Community Problem Solver makes it easy for communities to collaborate on local problems (streetlights, waste management, road repairs, etc.). The project pairs a React + Vite frontend with an Express + MongoDB backend and includes features for reporting issues, proposing solutions, voting, discussions, notifications, and volunteer coordination.

## Key Features

- User registration, login, and JWT-protected APIs
- Problem reporting with location, description, and photo support
- Solution proposals and an upvote system to surface helpful responses
- Discussion threads and activity tracking per problem
- Notifications for important user events
- Admin and volunteer flows for moderation and coordination

## Tech Stack

- Frontend: React, Vite, Tailwind CSS
- Backend: Node.js, Express, MongoDB, Mongoose
- Auth: JSON Web Tokens (JWT), bcrypt
- File uploads: multer + Cloudinary
- Email: nodemailer

## Repository Layout

```
client/    # React front-end
server/    # Express API server
```

## Prerequisites

- Node.js 18+ and npm
- A MongoDB connection (Atlas or self-hosted)
- (Optional) Cloudinary account for image uploads

## Installation

1. Backend

```bash
cd server
npm install
```

Create a `.env` in `server/` with these variables (example):

```env
MONGODB_URL=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret
CLOUD_NAME=your_cloudinary_cloud_name
API_KEY=your_cloudinary_api_key
API_SECRET=your_cloudinary_api_secret
SMTP_HOST=your_smtp_host
SMTP_PORT=your_smtp_port
SMTP_USER=your_smtp_user
SMTP_PASS=your_smtp_pass
FROM_EMAIL=your_from_email
FRONTEND_URL=http://localhost:5173
CORS_ORIGINS=http://localhost:5173
PORT=3000
```

Start the server in development:

```bash
npm run dev
```

2. Frontend

```bash
cd ../client
npm install
npm run dev
```

Visit `http://localhost:5173` to view the app.

## Seed Data (optional)

The repository contains a seed script to populate example problems, solutions, users, and notifications for local testing. Run it only in non-production environments after you set `MONGODB_URL`:

```bash
cd server
node scripts/seedMockData.js
```

Note: For security and privacy, credentials and any sensitive defaults are intentionally not included in this README.

## Contribution

Contributions are welcome. For this project, a good first step is improving documentation or making small UI/UX polish changes on the landing page. Typical workflow:

```bash
git checkout -b feature/your-change
# make edits (README.md for docs changes)
git add README.md
git commit -m "docs: improve README"
git push origin feature/your-change
# Open a PR against the main repository
```

If you were invited as a collaborator on the group repo, push your branch to the group repo and open a PR; otherwise fork the repo and open a PR from your fork.

## Available scripts

### Backend

- `npm run dev` — start server with nodemon
- `npm start` — run server

### Frontend (client)

- `npm run dev` — start Vite dev server
- `npm run build` — build production assets
- `npm run preview` — preview built frontend

## Notes

- Keep `.env` values out of version control.
- Use the seed script only for local testing — do not run it against production databases.

---

If you'd like, I can add screenshots, example API calls, or an architecture diagram in a follow-up commit.
