📌 Task Management System (Full-Stack)
A simple full-stack task manager built with Node.js, Prisma, PostgreSQL, and Next.js.
Includes authentication (JWT + Refresh Tokens), pagination, search, filters, and full CRUD.

🚀 Live URLs
Frontend (Vercel): [https://task-manager-frontend-pi-seven.vercel.app]
Backend (Railway): [https://task-manager-backend-v1.up.railway.app]

🛠 Tech Stack
Backend: Node.js, TypeScript, Express, Prisma, PostgreSQL, JWT, bcrypt
Frontend: Next.js (App Router), TypeScript, Axios, Tailwind CSS
Auth: Access Token + HTTP-Only Refresh Token

📦 Features
User Register / Login / Logout
Auto Refresh Token Handling
Create / Read / Update / Delete Tasks
Toggle Task Status
Pagination + Search + Status Filter
Task Stats (Total, Completed, In-Progress, Open)
Fully responsive dashboard


⚙️ Project Setup 
# Clone repo
git clone https://github.com/Siddhant7621/task-management-system

⚙️ Backend Setup (Node.js + Prisma)
1. navigate to backend
cd backend

2. Install dependencies
npm install

3. Environment variables

Create .env:

DATABASE_URL=postgresql://...
JWT_SECRET=your_jwt_secret
REFRESH_SECRET=your_refresh_secret
ACCESS_TOKEN_EXPIRES_IN=15m
REFRESH_TOKEN_EXPIRES_IN=7d
CLIENT_URL=http://localhost:3000

4. Prisma setup
npx prisma generate
npx prisma migrate dev --name init

5. Run backend
npm run dev

💻 Frontend Setup (Next.js)
1. navigate to frontend
cd task-manager-frontend

2. Install dependencies
npm install

3. Environment variables

Create .env.local:

NEXT_PUBLIC_API_URL=http://localhost:4000

4. Run frontend
npm run dev




✔ API Endpoints
Auth
POST /api/auth/register
POST /api/auth/login
POST /api/auth/refresh
POST /api/auth/logout

Tasks
GET /api/tasks
POST /api/tasks
GET /api/tasks/:id
PATCH /api/tasks/:id
DELETE /api/tasks/:id
POST /api/tasks/:id/toggle