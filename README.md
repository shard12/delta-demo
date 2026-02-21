# 🎓 Campus Grievance Redressal & Complaint Management System

> A **beginner-friendly, professional roadmap** to build this project using **VS Code + PowerShell**.
> 
> ✅ Rule we will follow: **Run locally first → push to GitHub → deploy live at the end**.

---

## 📌 What You Are Building

A role-based university grievance platform with:

- 👨‍🎓 **Student Portal** (submit & track complaints)
- 👨‍💼 **Department Admin Panel** (assign/manage complaints)
- 👨‍⚖️ **Higher Authority Panel** (handle escalations/final decisions)
- 📧 Email notifications
- 📊 Analytics dashboards
- 🔐 Secure authentication (JWT + bcrypt)

---

## 🎯 Project Objectives

- Digitize complaint handling
- Improve transparency and accountability
- Enable role-based access
- Reduce resolution delays
- Keep proper records and analytics

---

## 🧰 Recommended Tech Stack

### Frontend
- React + Vite
- Tailwind CSS
- React Router
- Recharts
- Lucide React (icons)

### Backend
- Node.js + Express.js
- MongoDB + Mongoose
- JWT + bcryptjs
- Nodemailer
- Multer (attachments)

### Tools
- VS Code
- PowerShell terminal
- Git + GitHub
- Postman

---

## 🗺️ Professional Development Plan (High Level)

1. Set up tools
2. Create project structure
3. Build and run locally ✅
4. Add authentication + role management
5. Add complaint workflow
6. Add notifications and analytics
7. Test properly
8. Push clean code to GitHub
9. Deploy live at the very end 🚀

---

## 0) ✅ Install Required Tools (Windows)

Open **PowerShell**:

```powershell
node -v
npm -v
git --version
```

If missing, install:
- Node.js LTS: https://nodejs.org
- Git: https://git-scm.com
- VS Code: https://code.visualstudio.com

Recommended VS Code extensions:
- ESLint
- Prettier
- Tailwind CSS IntelliSense
- GitLens

---

## 1) 📁 Create Project Structure

```powershell
mkdir campus-grievance-system
cd campus-grievance-system
mkdir client, server, docs
code .
```

Expected structure:

```text
campus-grievance-system/
  client/
  server/
  docs/
  README.md
```

---

## 2) ▶️ Local Deployment First (Important)

### 2.1 Frontend setup (React + Vite)

```powershell
npm create vite@latest client -- --template react
cd client
npm install
npm run dev
```

Open: `http://localhost:5173`

### 2.2 Backend setup (Express)

Open a second PowerShell terminal:

```powershell
cd ..\server
npm init -y
npm install express mongoose cors dotenv jsonwebtoken bcryptjs nodemailer multer
npm install -D nodemon
```

Create a basic server (`server.js`) and run:

```powershell
npx nodemon server.js
```

Open backend test URL (example): `http://localhost:5000/api/health`

> 🎯 First milestone: both frontend and backend run locally without errors.

---

## 3) 🧱 Build Core Modules (Step by Step)

### Module A: Authentication & Users
- Admin-created accounts only (no public signup)
- Login by role (Student/Admin/Authority)
- JWT auth + protected routes
- Forgot password with email reset

### Module B: Complaint Management
- Category: Academics / Faculty / Infrastructure / Administration
- Priority: Low / Medium / High
- Status workflow:
  - Pending
  - Assigned
  - In Progress
  - Escalated
  - Resolved
- Attachment upload
- Complaint history and timeline

### Module C: Admin Controls
- Assign complaints
- Add internal remarks
- Update statuses
- Official resolution response

### Module D: Dashboards & Analytics
- Total/Pending/Resolved cards
- Category pie chart
- Monthly trend chart
- Resolution time metrics

### Module E: Professional Add-ons
- SLA timer
- Auto-escalation
- CSV export
- Audit trail (who changed what, when)

---

## 4) 🎨 UI/UX Standards (Professional)

Use a modern dashboard style:

- Sidebar + top navbar
- Icons in navigation and action buttons
- Search, filter, pagination
- Responsive layout
- Color-coded statuses:
  - 🟡 Pending
  - 🔵 In Progress
  - 🔴 Escalated
  - 🟢 Resolved

---

## 5) 🔐 Security Checklist

- Hash passwords with `bcryptjs`
- Sign/verify tokens with `jsonwebtoken`
- Role-based middleware protection
- Validate/sanitize inputs
- Restrict file types and size in uploads
- Keep secrets in `.env`
- Never commit `.env` to GitHub

---

## 6) 📧 Email Notification Checklist

Trigger emails when:

- Complaint submitted
- Complaint assigned
- Status changed
- Escalated
- Resolved (with official message)
- Password reset requested

---

## 7) 🧪 Testing Checklist

Run these before each push:

```powershell
# frontend
cd client
npm run dev
npm run build

# backend
cd ..\server
npx nodemon server.js
```

Manual checks:
- [ ] Role login works
- [ ] Protected routes blocked for unauthorized users
- [ ] Complaint create/update works
- [ ] Attachments upload correctly
- [ ] Email notifications trigger
- [ ] Escalation flow works
- [ ] UI is responsive

---

## 8) 🐙 GitHub Workflow (Store Everything Properly)

From project root:

```powershell
git init
git add .
git commit -m "chore: initial project setup"
git branch -M main
git remote add origin https://github.com/<your-username>/<repo-name>.git
git push -u origin main
```

After each feature:

```powershell
git add .
git commit -m "feat: add complaint workflow"
git push
```

Create professional docs:
- `README.md`
- `.gitignore`
- `docs/API.md`
- `docs/DB_SCHEMA.md`
- `LICENSE`

---

## 9) 🌍 Live Deployment (Do This Last)

> Only after local build is stable and tested.

Recommended hosting:
- Frontend: Vercel / Netlify
- Backend: Render / Railway
- Database: MongoDB Atlas

Deployment order:
1. Push final tested code to GitHub
2. Deploy backend and verify APIs
3. Add backend URL to frontend env
4. Deploy frontend
5. Verify complete complaint lifecycle on live URL

Deliverables:
- Live URL
- GitHub repository URL
- Screenshots
- Demo video

---

## 10) 📄 University Report-Ready Sections

Use these chapter headings directly:

- Abstract
- Problem Statement
- Objectives
- Existing vs Proposed System
- Module Design
- Tech Stack
- Database/ER Diagram
- Security Features
- Testing
- Results
- Future Scope
- Conclusion

---

## 💼 Resume-Ready Line

> Developed a role-based Campus Grievance Redressal System with JWT authentication, complaint workflow automation, role-based dashboards, email notifications, and analytics for university administration.

---

## 🆘 Beginner Troubleshooting (VS Code + PowerShell)

### `npm` not recognized
Close VS Code, reopen PowerShell, run:

```powershell
node -v
npm -v
```

### Port already in use

```powershell
npm run dev -- --port 5174
```

### Git push rejected

```powershell
git pull origin main --rebase
git push
```

### Wrong terminal in VS Code
VS Code → **Terminal** → **Select Default Profile** → **PowerShell**

---

## ✅ Final Advice

- Build one module at a time.
- Test locally every day.
- Commit frequently with clean messages.
- Keep screenshots and notes for final viva/report.
- Do **local deployment first**, then GitHub, then live deployment.

You are absolutely on the right path — this can become a top-quality academic project. 🚀
