# TaskFlow — MERN Task Manager with CI/CD Pipeline

A full-stack task management app built with the MERN stack, containerised with Docker and deployed on AWS EC2 via a fully automated GitHub Actions CI/CD pipeline. Built this to learn what it actually takes to ship something to production properly — not just make it work locally.


---

## 🚀 Features

- ✅ Create, read, update, and delete tasks
- 🎨 Modern dark theme with glassmorphism effects
- 📱 Fully responsive design
- 🔒 TypeScript for end-to-end type safety
- 🐳 Dockerised with multi-stage builds for lean production images
- 🔄 Automated CI/CD — push to main, live in under 3 minutes

---

## 🛠️ Tech Stack

**Frontend:** React 18 · TypeScript · TailwindCSS · Axios  
**Backend:** Node.js · Express.js · MongoDB · Mongoose  
**DevOps:** Docker · GitHub Actions · AWS EC2 · Nginx · AWS CloudWatch  

---

## 🔄 CI/CD Pipeline

Every push to `main` automatically:

1. Builds optimised Docker image via multi-stage Dockerfile
2. Pushes versioned image to Docker Hub
3. SSH-deploys to AWS EC2
4. Restarts container with latest image

Deployment time went from ~15 minutes of manual work down to under 3 minutes automatically.

---

## ⚙️ Infrastructure

- 🐳 **Docker** — multi-stage builds to keep production images lean
- 🔄 **GitHub Actions** — automated build, push and deploy pipeline
- ☁️ **AWS EC2** — production server hosting the containerised app
- 🌐 **Nginx** — reverse proxy with HTTPS via Let's Encrypt
- 🗂️ **Docker Hub** — image registry with version tagging for rollbacks
- 📊 **AWS CloudWatch** — CPU/memory alarms and centralised log monitoring

---

## 📦 Local Setup

### Option A: Docker (Recommended)

```bash
# Clone the repo
git clone https://github.com/Pranav-exe/taskflow.git
cd taskflow

# Configure environment variables
cp server/.env.example server/.env
# Fill in your MongoDB URI, JWT secret etc.

# Start with Docker
docker compose up --build
```

- Frontend: `http://localhost:3000`  
- Backend API: `http://localhost:4000`

### Option B: Manual Setup

```bash
npm run install-all
npm start
```

---

## 📁 Project Structure
taskflow/
├── client/                 # React frontend
│   ├── src/
│   │   ├── components/    # React components
│   │   ├── services/      # API services
│   │   └── styles/        # CSS and styling
│   └── package.json
├── server/                 # Express backend
│   ├── models/            # MongoDB models
│   ├── routes/            # API routes
│   ├── controllers/       # Route controllers
│   └── package.json
├── .github/
│   └── workflows/
│       └── deploy.yml     # GitHub Actions CI/CD pipeline
└── docker-compose.yml
---

## 🎯 Usage

1. **Add a Task** — click the Add button or press Enter
2. **Complete a Task** — click the checkbox to mark as done
3. **Edit a Task** — click the edit icon to modify
4. **Delete a Task** — click the delete icon to remove

---

## 👨‍💻 Author

**Pranav Sharma**  
[GitHub](https://github.com/Pranav-exe) ·

---

⭐ Star this repo if you found it useful!
