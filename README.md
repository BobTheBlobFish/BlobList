📁 Project Management Dashboard – Complete Build
This repository contains the full codebase for a Project Management Dashboard built with modern web technologies, integrating scalable cloud services and real-time functionality. It includes setup instructions, environment configuration, and deployment steps for a complete end-to-end project.

🧰 Tech Stack
Frontend:

Next.js

Tailwind CSS

Redux Toolkit & Redux Toolkit Query

Material UI Data Grid

Backend:

Node.js with Express

Prisma ORM (PostgreSQL)

Database:

PostgreSQL, managed via PgAdmin

Cloud & DevOps:

AWS EC2, RDS, API Gateway, Amplify, S3, Lambda, Cognito

⚙️ Getting Started
✅ Prerequisites
Ensure the following are installed on your system:

Git

Node.js

npm

PostgreSQL

PgAdmin

📦 Installation
Clone the repository:

bash
Copy
Edit
git clone [repo-url]
cd project-management
Install dependencies for both frontend and backend:

bash
Copy
Edit
cd client
npm install
cd ../server
npm install
Set up the database:

bash
Copy
Edit
npx prisma generate
npx prisma migrate dev --name init
npm run seed
Configure environment variables:

server/.env – for PORT, DATABASE_URL

client/.env.local – for NEXT_PUBLIC_API_BASE_URL

Start the development servers:

bash
Copy
Edit
npm run dev
📚 Additional Resources
Complete code and configuration files

Tailwind config & global styles (globals.css)

Redux Toolkit setup

Seed files and sample data

Gantt chart styling and dependencies

🗃 Database Management
To reset a PostgreSQL ID sequence:

sql
Copy
Edit
SELECT setval(
  pg_get_serial_sequence('"[DATA_MODEL_NAME_HERE]"', 'id'),
  coalesce(max(id)+1, 1),
  false
) FROM "[DATA_MODEL_NAME_HERE]";


NOTE: The application is currently facing an issue due to an AWS change with Cognito. Deployed AWS URL is- https://main.d1r9lkqxzptla.amplifyapp.com
