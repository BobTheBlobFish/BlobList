# 🗂️ Project Management Dashboard

This repository contains a complete **Project Management Dashboard** built using modern full-stack technologies. It features a powerful frontend, a scalable backend, PostgreSQL database integration, and deployment-ready configuration with AWS cloud services.

---

## 🧰 Tech Stack

### Frontend
- **Next.js 15**
- **React 19**
- **Tailwind CSS**
- **Redux Toolkit & Redux Toolkit Query**
- **Material UI Data Grid**

### Backend
- **Node.js** with **Express**
- **Prisma** (ORM for PostgreSQL)

### Database
- **PostgreSQL**, managed via **PgAdmin**

### Cloud Infrastructure
- **AWS EC2** (Application Hosting)
- **AWS RDS** (PostgreSQL Database)
- **AWS S3** (File Storage)
- **AWS Lambda** (Serverless Functions)
- **AWS Amplify** (Frontend Hosting)
- **AWS API Gateway** (API Management)
- **AWS Cognito** (User Authentication)

---

## ⚙️ Getting Started

Follow the steps below to set up the project locally.

### ✅ Prerequisites

Ensure the following tools are installed on your system:

- [Git](https://git-scm.com/)
- [Node.js & npm](https://nodejs.org/)
- [PostgreSQL](https://www.postgresql.org/)
- [PgAdmin](https://www.pgadmin.org/)

---

### 📥 Installation & Setup

```bash
# 1. Clone the repository
git clone [your-repo-url]
cd project-management

# 2. Install dependencies

# For client
cd client
npm install

# For server
cd ../server
npm install

# 3. Set up the database
npx prisma generate
npx prisma migrate dev --name init
npm run seed

# 4. Configure environment variables

# Create server/.env with the following:
PORT=8000
DATABASE_URL=postgresql://<username>:<password>@<host>:5432/<db_name>

# Create client/.env.local with the following:
NEXT_PUBLIC_API_BASE_URL=http://localhost:8000

# 5. Start the development servers

# Start the backend
cd server
npm run dev

# In a new terminal, start the frontend
cd ../client
npm run dev 
```
**NOTE** : The application is currently facing an authorization bug due to an AWS Cognito update, which resulting in users not being able to login. Here is the link deployed on Amplify AWS anyways: https://main.d1r9lkqxzptla.amplifyapp.com
