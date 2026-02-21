# 🎓 Campus Grievance Redressal & Complaint Management System

A beginner-friendly, professional, step-by-step guide to build and deploy your university-level project using **VS Code + PowerShell**.

---

## 📚 Table of Contents

1. [Project Overview](#-project-overview)
2. [Objectives](#-objectives)
3. [User Roles](#-user-roles)
4. [Tech Stack (Recommended)](#-tech-stack-recommended)
5. [Professional Features Checklist](#-professional-features-checklist)
6. [Development Roadmap (Step-by-Step)](#-development-roadmap-step-by-step)
7. [Step 0: Install Tools on Windows](#-step-0-install-tools-on-windows)
8. [Step 1: Set Up Project Folder in VS Code](#-step-1-set-up-project-folder-in-vs-code)
9. [Step 2: Run Project Locally (FIRST)](#-step-2-run-project-locally-first)
10. [Step 3: Create a Professional Frontend](#-step-3-create-a-professional-frontend)
11. [Step 4: Build Backend API](#-step-4-build-backend-api)
12. [Step 5: Connect Frontend + Backend](#-step-5-connect-frontend--backend)
13. [Step 6: Add Authentication & Security](#-step-6-add-authentication--security)
14. [Step 7: Add Complaint Workflow](#-step-7-add-complaint-workflow)
15. [Step 8: Add Email Notifications](#-step-8-add-email-notifications)
16. [Step 9: Add Analytics Dashboard](#-step-9-add-analytics-dashboard)
17. [Step 10: Test Like a Professional](#-step-10-test-like-a-professional)
18. [Step 11: Push Everything to GitHub](#-step-11-push-everything-to-github)
19. [Step 12: Deploy Live (AT THE END)](#-step-12-deploy-live-at-the-end)
20. [Project Proposal / Report Content](#-project-proposal--report-content)
21. [Resume-Ready Project Line](#-resume-ready-project-line)
22. [Troubleshooting for Beginners](#-troubleshooting-for-beginners)

---

## 📌 Project Overview

The **Campus Grievance Redressal & Complaint Management System** is a role-based web application where:

- 👨‍🎓 Students can submit and track complaints.
- 👨‍💼 Department Admins can assign/manage complaints.
- 👨‍⚖️ Higher Authority can handle escalations and final decisions.

This replaces manual complaint handling with a transparent digital system.

---

## 🎯 Objectives

- Digitize grievance submission.
- Enable role-based secure access.
- Support category + priority handling.
- Provide status tracking and complaint history.
- Send automated email notifications.
- Offer analytics for institutional monitoring.

---

## 👥 User Roles

### 1) 👨‍🎓 Student

- Login securely
- Submit complaint (Academics / Faculty / Infrastructure / Administration)
- Set priority: Low / Medium / High
- Upload files/images
- Track status
- Receive email updates

### 2) 👨‍💼 Department Admin

- View department complaints
- Assign complaints
- Update status: Pending / In Progress / Escalated / Resolved
- Add remarks and official response
- Monitor timelines
- Export reports

### 3) 👨‍⚖️ Higher Authority

- View escalated cases
- Override decisions
- Mark final resolution
- Monitor system-wide analytics

---

## 🧰 Tech Stack (Recommended)

### Frontend
- React + Vite
- Tailwind CSS
- React Router
- Recharts (for analytics)
- Lucide React / Font Awesome (icons)

### Backend
- Node.js + Express.js
- MongoDB + Mongoose
- JWT + bcrypt
- Nodemailer
- Multer (file upload)

### Dev Tools
- VS Code
- PowerShell Terminal
- Postman
- Git + GitHub

---

## ✅ Professional Features Checklist

- [ ] Role-based dashboards
- [ ] JWT auth + protected routes
- [ ] Forgot password via email
- [ ] Complaint status workflow
- [ ] Complaint ID generation
- [ ] File attachments
- [ ] Email notifications
- [ ] CSV export
- [ ] Analytics charts
- [ ] Audit logs
- [ ] SLA timer + auto-escalation
- [ ] Responsive UI + status badges

---

## 🛣 Development Roadmap (Step-by-Step)

You should follow this exact order:

1. Install tools
2. Create project structure
3. **Run locally first** ✅
4. Build frontend UI
5. Build backend API
6. Connect frontend/backend
7. Add auth/security
8. Add complete complaint workflow
9. Push to GitHub regularly
10. Test and polish
11. **Deploy live at the very end** 🚀

---

## 🧩 Step 0: Install Tools on Windows

Open **PowerShell** and run:

```powershell
node -v
git --version
python --version
```

If any command fails, install:

- Node.js LTS: https://nodejs.org
- Git: https://git-scm.com
- Python: https://python.org (optional but useful)
- VS Code: https://code.visualstudio.com

Recommended VS Code extensions:

- ES7+ React Snippets
- Prettier
- ESLint
- Tailwind CSS IntelliSense
- GitLens

---

## 🗂 Step 1: Set Up Project Folder in VS Code

```powershell
mkdir campus-grievance-system
cd campus-grievance-system
code .
```

Create project structure:

```text
campus-grievance-system/
  client/
  server/
  docs/
  README.md
```

---

## ▶️ Step 2: Run Project Locally (FIRST)

### Option A: If using React + Vite frontend

```powershell
npm create vite@latest client -- --template react
cd client
npm install
npm run dev
```

Open browser: `http://localhost:5173`

### Option B: If testing static HTML quickly

From project root:

```powershell
python -m http.server 5500
```

Open browser: `http://localhost:5500`

> ✅ First success target: Your app opens on localhost without errors.

---

## 🎨 Step 3: Create a Professional Frontend

Build these screens first:

- Login Page (no public signup)
- Student Dashboard
- Department Admin Dashboard
- Higher Authority Dashboard
- Complaint Submit Form
- Complaint List + Filters
- Complaint Details + Timeline

UI guidelines:

- Use sidebar + top navbar
- Add icons for each menu
- Use badges:
  - 🟡 Pending
  - 🔵 In Progress
  - 🔴 Escalated
  - 🟢 Resolved
- Keep spacing consistent and modern
- Make it mobile responsive

---

## ⚙️ Step 4: Build Backend API

Inside `server`:

```powershell
mkdir server
cd server
npm init -y
npm install express mongoose cors dotenv jsonwebtoken bcryptjs nodemailer multer
npm install -D nodemon
```

Create folders:

```text
server/
  src/
    config/
    controllers/
    middleware/
    models/
    routes/
    utils/
    app.js
    server.js
  .env
  package.json
```

Initial server run command:

```powershell
npm run dev
```

---

## 🔗 Step 5: Connect Frontend + Backend

- Use Axios or Fetch from frontend.
- Keep API base URL in `.env`.
- Test each endpoint with Postman first.

Example flow:

1. Login API works
2. Store JWT
3. Send token in protected API requests
4. Load complaints role-wise

---

## 🔐 Step 6: Add Authentication & Security

Must implement:

- bcrypt password hashing
- JWT access tokens
- Role-based route guards
- Forgot password link via email
- Reset token expiry
- Basic input validation and sanitization

Security best practices:

- Never commit `.env`
- Use strong secret keys
- Validate file uploads
- Add rate limiting later

---

## 📝 Step 7: Add Complaint Workflow

Complaint fields:

- Complaint ID (e.g., CMP-2025-0001)
- Student details
- Category
- Priority
- Description
- Attachments
- Current status
- Assigned admin
- Remarks
- Resolution message
- Timestamps

Workflow statuses:

`Pending → Assigned → In Progress → Escalated → Resolved`

---

## 📧 Step 8: Add Email Notifications

Send emails on:

- Complaint submitted
- Complaint assigned
- Status changed
- Escalated
- Resolved with official response
- Password reset

Tip: Use Gmail App Password or Mailtrap for testing.

---

## 📊 Step 9: Add Analytics Dashboard

Add charts/cards for:

- Total complaints
- Pending count
- Resolved count
- Average resolution time
- Category-wise pie chart
- Monthly trend graph
- Department-wise summary

---

## 🧪 Step 10: Test Like a Professional

Minimum testing checklist:

- [ ] Login with each role
- [ ] Unauthorized route blocked
- [ ] Complaint create/update works
- [ ] Email notifications triggered
- [ ] Escalation logic works
- [ ] File upload works
- [ ] Mobile view tested
- [ ] No sensitive data exposed

Useful commands:

```powershell
npm run dev
npm run build
npm run lint
```

---

## 🐙 Step 11: Push Everything to GitHub

From project root in PowerShell:

```powershell
git init
git add .
git commit -m "Initial professional setup"
git branch -M main
git remote add origin https://github.com/<your-username>/<repo-name>.git
git push -u origin main
```

After each major feature:

```powershell
git add .
git commit -m "Add complaint workflow module"
git push
```

Create these files for professionalism:

- `README.md`
- `.gitignore`
- `docs/API.md`
- `docs/DB_SCHEMA.md`
- `LICENSE`

---

## 🌍 Step 12: Deploy Live (AT THE END)

> 🚨 Do this only after local project is fully stable.

Suggested deployment:

- Frontend (React): **Vercel** or **Netlify**
- Backend (Node): **Render** or **Railway**
- Database: **MongoDB Atlas**

Deployment flow:

1. Push latest code to GitHub
2. Add production environment variables
3. Deploy backend first
4. Add backend URL to frontend `.env`
5. Deploy frontend
6. Test full login + complaint cycle on live URL

Final deliverables:

- Live project URL
- GitHub repo URL
- Screenshots for report
- Demo video

---

## 🧾 Project Proposal / Report Content

You can directly use these sections in your report:

- Abstract
- Problem Statement
- Objectives
- Existing vs Proposed System
- Modules
- Technology Stack
- Database Design (ER Diagram)
- Security Features
- Testing Strategy
- Future Scope
- Conclusion

---

## 💼 Resume-Ready Project Line

> Developed a role-based Campus Grievance Redressal System with secure authentication, complaint workflow automation, email notifications, analytics dashboards, and escalation handling for university-level administration.

---

## 🆘 Troubleshooting for Beginners

### `npm` not recognized
Reopen terminal after Node installation.

### Port already in use
Run app on another port:

```powershell
npm run dev -- --port 5174
```

### Git push rejected
Pull first, then push:

```powershell
git pull origin main --rebase
git push
```

### VS Code terminal mismatch
In VS Code: **Terminal → Select Default Profile → PowerShell**

---

## 🙌 Final Advice

- Build slowly, module by module.
- Commit code every day.
- Keep screenshots for each completed feature.
- First local success, then GitHub, then live deployment.

You are building a strong professional project — keep going! 🚀
