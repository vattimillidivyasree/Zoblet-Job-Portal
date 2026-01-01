
 # 💼 Zoblet — Jobs, Reimagined (MERN Stack)
<br/>
Zoblet is a full-stack job portal application built with the MERN stack that redefines the hiring experience. Using MongoDB, Express.js, React.js, and Node.js, it delivers secure authentication, role-based access control, dynamic job listings, and seamless application tracking — all within a fast, responsive, and scalable web platform.
<br/>

 ## 🌐 Live Demo (DEPLOYED):<br/>
https://zoblet-web-client.vercel.app/
 <br/>

 ## 📎 What Zoblet Offers

<br/>  
Secure authentication and role-based access using Clerk 
<br/>  
Employer-focused job posting and management built on the MERN stack  
<br/>  
Fast and efficient job search powered by MongoDB  
<br/>  
Simple job application and application status tracking  
<br/>  
Dedicated dashboards for recruiters and candidates using React  
<br/>  
Resume and profile uploads handled via Cloudinary  
<br/>  
Responsive, mobile-first UI styled with Tailwind CSS  
<br/>  
Scalable RESTful APIs using Node.js and Express.js  
<br/>

## 🧩 Technology Overview
<br/>
Client: React (Vite) with modern JSX and Tailwind styling
<br/>
Server: Express-powered Node.js backend
<br/>
Data Layer: MongoDB with Mongoose ODM
<br/>
Auth System: Clerk for secure identity & access control
<br/>
Media Handling: Cloudinary for document and image storage
<br/>
Observability: Sentry for real-time error and performance tracking
<br/>
API Design: Scalable REST architecture with protected routes
<br/>
Hosting & Delivery: Vercel for seamless cloud deployment
<br/>

## 🔧 Installation & Setup

 1. Clone the repository
```bash
git clone https://github.com/vattimillidivyasree/Zoblet.git
cd Zoblet
```

2. 📥 Environment Variables on server side
<br/>
Create a `.env` file inside the server folder with the following variables: 

```bash
JWT_SECRET="dev#secret"

# MongoDb Setup
MONGODB_URI = '----- MongoDB URI -----'

# Cloudinary Setup
CLOUDINARY_NAME = '----- Cloudinary Name -----'
CLOUDINARY_API_KEY = '----- Cloudinary API Key -----'
CLOUDINARY_SECRET_KEY = '----- Cloudinary Secret Key -----'

# Clerk Setup
CLERK_WEBHOOK_SECRET = '----- Clerk Webhook Secret -----'
CLERK_PUBLISHABLE_KEY = '----- Clerk Publishable Key -----'
CLERK_SECRET_KEY = '----- Clerk Secret Key -----'
```
3.📥 Environment Variables on client side
<br/>
Create a `.env` file inside the client folder with the following variables: 

```bash
VITE_CLERK_PUBLISHABLE_KEY= '----- Clerk Publishable Key -----'
VITE_BACKEND_URL = 'http://localhost:5000'
```
4.Start the backend server and run the frontend client:
```bash
npm install
npm run dev
```

## 🧩 Prerequisites
<br/><br/>

• Node.js (v18 or higher recommended)  
<br/>
• npm or yarn package manager  
<br/>
• MongoDB (local setup or MongoDB Atlas)  
<br/>
• Clerk account for authentication & role management  
<br/>
• Cloudinary account for resume & profile uploads  
<br/>
• Sentry account for error monitoring (optional but recommended)  
<br/>
• Git & GitHub for version control and deployment  
<br/>
• Modern web browser (Chrome / Edge / Firefox)  
<br/>
• Code editor (VS Code recommended)  
<br/>

## 📦 Dependencies <br/><br/>

### 💻 Frontend <br/>

- `@clerk/clerk-react` : `^5.17.1` <br/>
- `axios` : `^1.7.9` <br/>
- `k-convert` : `^1.0.6` <br/>
- `moment` : `^2.30.1` <br/>
- `quill` : `^2.0.3` <br/>
- `react` : `^18.3.1` <br/>
- `react-dom` : `^18.3.1` <br/>
- `react-router-dom` : `^7.0.1` <br/>
- `react-toastify` : `^10.0.6` <br/>

###  🪛Backend <br/>

- `@clerk/express` : `^1.3.21` <br/>
- `@sentry/node` : `^8.42.0` <br/>
- `@sentry/profiling-node` : `^8.42.0` <br/>
- `bcrypt` : `^5.1.1` <br/>
- `cloudinary` : `^2.5.1` <br/>
- `cors` : `^2.8.5` <br/>
- `dotenv` : `^16.4.7` <br/>
- `express` : `^4.21.1` <br/>
- `jsonwebtoken` : `^9.0.2` <br/>
- `mongoose` : `^8.8.3` <br/>
- `multer` : `^1.4.5-lts.1` <br/>
- `svix` : `^1.42.0` <br/>

### ⚙️ Dev Tools <br/>

- `nodemon` : `^3.1.7` <br/>

## 🔁 Job Flow <br/><br/>

1. Sign Up & Login <br/>
Users register or log in securely using Clerk authentication <br/><br/>

2. Browse Jobs <br/>
Candidates explore all job listings and filter by role, company, or keywords <br/><br/>

3. Apply & Track <br/>
Candidates submit applications and track their status in real-time <br/><br/>

4. Recruiter Dashboard <br/>
Recruiters post, manage, and update job listings via the dashboard <br/><br/>

5. Candidate Management <br/>
Recruiters review profiles, resumes (uploaded via Cloudinary), and manage applications <br/>

## 🔌 API Endpoints <br/><br/>

### Authentication <br/>
Authentication is handled via **Clerk**. <br/>
No custom login/register endpoints are implemented <br/><br/>

### Jobs <br/>
- GET `/api/jobs` – Get all job listings <br/>
- GET `/api/jobs/:id` – Get job details <br/>
- POST `/api/jobs` – Create a job (Recruiter) <br/><br/>

### Applications <br/>
- POST `/api/apply` – Apply to a job <br/>
- GET `/api/applications` – View my applications <br/><br/>

### Candidates <br/>
- GET `/api/candidates/:jobId` – View applicants for a job (Recruiter) <br/>

## ⚡ Troubleshooting & Tips <br/><br/>

### Server Issues <br/>
- Make sure MongoDB URI is correctly set in `.env` <br/>
- Verify that the backend port is not already in use <br/><br/>

### Authentication Issues <br/>
- Check Clerk API keys and secrets are correct <br/>
- Ensure allowed origins are set properly in the Clerk dashboard <br/><br/>

### Job & Application Issues <br/>
- Verify job creation, editing, and application endpoints <br/>
- Check that application status updates are working correctly <br/>
-Checking cloudinary updates if resumes are failing <br/><br/>git add
### Frontend Issues <br/>
- Run `npm install` in the client folder before starting <br/>
- Confirm the backend server is running and API URLs are correct <br/>

## 🔍 Testing & Validation <br/><br/>

- Ensure users can register and log in securely via Clerk <br/>
- Confirm recruiters can create, update, and remove job listings <br/>
- Verify candidates can apply to jobs and track application status <br/>
- Test role-based access to protect candidate vs recruiter routes <br/>
- Inspect API endpoints and responses using tools like Postman <br/>
- Check data integrity for jobs, applications, and user profiles <br/>

 ## 📄  License <br/>
This project is licensed under the MIT License. <br/><br/>


## 🌟 Upcoming Features <br/><br/>
• AI-powered job recommendations for candidates <br/>
• Advanced analytics dashboard for recruiters <br/>
• Streamlined application workflow with notifications <br/>

## ✨ How to Contribute <br/><br/>
Contributions are currently not accepted for this project. <br/>
This repository is maintained as a completed full-stack project for learning and portfolio purposes. <br/>

## 💡 Credits & Thanks <br/><br/>
- **Clerk** for authentication and role management <br/>
- **MongoDB** for database services <br/>
- **Cloudinary** for resume and media storage <br/>
- **Sentry** for error tracking and monitoring <br/>
- **React & Node.js** open-source community <br/>


# React + Vite

This template provides a minimal setup to get React working in Vite with HMR and some ESLint rules.<br/>

Currently, two official plugins are available:<br/>

- [@vitejs/plugin-react](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react/README.md) uses [Babel](https://babeljs.io/) for Fast Refresh<br/>
- [@vitejs/plugin-react-swc](https://github.com/vitejs/vite-plugin-react-swc) uses [SWC](https://swc.rs/) for Fast Refresh<br/>
