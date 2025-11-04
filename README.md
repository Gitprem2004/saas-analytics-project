# SaaS Analytics Project

An AI-powered analytics assistant for SaaS businesses. This tool allows you to ask questions in plain English and instantly receive SQL queries, data visualizations, and actionable insights.

> ⚠️ Currently runs **locally only**. Not deployed online yet.
> Future plan: Deploy Backend (Railway) & Frontend (Vercel)

---

## 🚀 Features

✅ Natural Language to SQL Query Conversion  
✅ AI-Generated Insights using Google Gemini  
✅ Interactive Visualizations (Pie/Bar charts)  
✅ Query History & CSV Export  
✅ Ready-to-use Sample SaaS Dataset  
✅ Full-Stack Solution (React + FastAPI + SQLite)

---

## 🏗️ Tech Stack

### Frontend
- React with TypeScript
- Chart.js
- Axios
- Responsive CSS

### Backend
- FastAPI
- SQLAlchemy ORM
- SQLite
- Google Gemini Pro API

---

## 🔌 Architecture

Frontend (React)  
⬇  
Backend API (FastAPI)  
⬇  
Gemini AI → SQL Generation  
⬇  
Database → Query Results + Insights

---

## 🖥️ Local Setup Guide

### ✅ Prerequisites
- Python 3.11+
- Node.js 18+
- Git installed

---

### 🔹 Backend Setup
```bash
cd backend
pip install -r requirements.txt
cp .env.example .env
# Add your GEMINI_API_KEY in .env
uvicorn app.main:app --reload --port 8000

✅ API Docs available at → http://localhost:8000/docs
✅ Optional sample data loading → http://localhost:8000/api/generate-data

### 🔹 frontend setup

cd frontend
npm install
cp .env.example .env
npm start

**🔑 Environment Variables**
**Backend .env**
GEMINI_API_KEY=your_key_here
DATABASE_URL=sqlite:///./saas_analytics.db
ENVIRONMENT=development

---

## 🖥️ Local Development Setup

### ✅ Prerequisites

| Requirement | Version |
|------------|---------|
| Python | 3.11 or higher |
| Node.js | 18 or higher |
| Git | Latest |

---

### 🔹 Backend Setup

```bash
cd backend
pip install -r requirements.txt
cp .env.example .env
# Add your GEMINI_API_KEY in .env
uvicorn app.main:app --reload --port 8000

### frontend .env
REACT_APP_API_URL=http://localhost:8000

| Method | Endpoint                   | Description                |
| ------ | -------------------------- | -------------------------- |
| GET    | `/`                        | Health check               |
| POST   | `/api/query`               | AI Query + SQL Execution   |
| POST   | `/api/generate-data`       | Create sample SaaS dataset |
| POST   | `/api/initialize-database` | Setup database schema      |
| GET    | `/docs`                    | Swagger UI                 |

**Project folder structure**
saas-analytics-project/
│
├── backend/
│   ├── app/
│   │   ├── main.py
│   │   ├── config.py
│   │   ├── database.py
│   │   ├── models/
│   │   └── services/
│   ├── requirements.txt
│   └── .env
│
├── frontend/
│   ├── src/
│   ├── package.json
│   └── .env
│
└── README.md


🔮 Future Enhancements

User Authentication & Access Roles

PostgreSQL / MySQL Cloud DB

Advanced SaaS Dashboards (Retention, LTV, NPS)

Export as PDF Reports

Real-Time Streaming Data

Scheduled Email Reports

👤 Author

Premkumar S

GitHub: https://github.com/Gitprem2004

LinkedIn: https://www.linkedin.com/in/prem19

Email: premkarthik30@gmail.com
