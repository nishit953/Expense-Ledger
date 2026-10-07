# 💰 ExpenseLedger

An AI-powered personal finance platform to track expenses, manage budgets, set savings goals, and get smart financial insights. Built as my Semester 4 project.

**Frontend:** React (Vite) + Tailwind CSS  
**Backend:** Django REST Framework + SQLite

---

## ✨ Features

- 🔐 **Authentication** – register, login, JWT tokens, email OTP verification, forgot/reset password
- 💸 **Expenses & Income** – full CRUD with search, filters, sorting, pagination and receipt upload
- 📊 **Budgets** – per-category monthly budgets with live progress tracking
- 🏦 **Savings** – savings entries, growth chart and emergency fund tracking
- 🎯 **Goals** – create goals, add contributions, track progress and completion
- 📈 **Dashboard & Analytics** – net worth, financial health score, trends, upcoming bills, weekly spending patterns
- 🧾 **Reports** – monthly / yearly / custom reports with **PDF and Excel export**
- 🔔 **Notifications** – budget alerts, goal reminders, bill reminders, low-savings alerts
- 🤖 **AI Insights (ML)** – expense category suggestion, overspending risk, next-month forecast, unusual-transaction detection, goal-completion forecast
- ⚙️ **Settings & Profile** – dark/light theme, currency, language, notification preferences, avatar

---

## 🛠️ Tech Stack

| Layer | Technologies |
|---|---|
| Frontend | React 18, Vite, Tailwind CSS, React Router, Framer Motion, Recharts, Axios, React Hook Form |
| Backend | Django 5, Django REST Framework, SimpleJWT, django-filter, django-cors-headers |
| Database | SQLite |
| ML / Reports | scikit-learn, pandas, numpy, joblib, ReportLab, OpenPyXL |

---

## 📁 Project Structure

```
ExpenseLedgerAntigrevity/
├── expense-ledger/            # React frontend
│   └── src/ (components, pages, hooks, services, context, utils)
└── expense-ledger-backend/    # Django backend
    ├── config/                # settings & root urls
    └── apps/                  # authentication, expenses, income, budgets, savings,
                               # goals, dashboard, analytics, reports,
                               # notifications, settings_app, ml, insights
```

---

## 🚀 Getting Started

### 1. Backend

```bash
cd ExpenseLedgerAntigrevity/expense-ledger-backend
python -m venv venv
venv\Scripts\activate            # Mac/Linux: source venv/bin/activate
pip install -r requirements.txt
cp .env.example .env             # then edit values
python manage.py migrate
python manage.py createsuperuser
python manage.py runserver
```

API runs at `http://localhost:8000/api/` (admin at `/admin/`).  
> In development, OTP / reset emails print in the terminal console.

### 2. Frontend

```bash
cd ExpenseLedgerAntigrevity/expense-ledger
npm install
cp .env.example .env             # VITE_API_BASE_URL=http://localhost:8000/api
npm run dev
```

Open `http://localhost:5173`.

### 3. (Optional) Train ML models

```bash
python manage.py train_ml_models --model all
```

Until models are trained, predictions use built-in rule-based fallbacks.

---

## 🔌 API Overview

| Endpoint | Purpose |
|---|---|
| `/api/auth/` | Register, login, profile, password reset |
| `/api/expenses/` · `/api/income/` | Transactions |
| `/api/budgets/` · `/api/savings/` · `/api/goals/` | Planning & saving |
| `/api/dashboard/` · `/api/analytics/` | Summaries and charts |
| `/api/reports/` | Reports + PDF/Excel export |
| `/api/notifications/` · `/api/settings/` | Alerts & preferences |
| `/api/ml/` · `/api/insights/` | ML predictions & AI insights |

---

## 📸 Screenshots

_Add screenshots of the dashboard, expenses page, and reports here._

---

## 🔮 Future Improvements

- Deploy frontend and backend online
- Scheduled notifications (task queue)
- Switch to PostgreSQL for production
- Mobile-friendly app / PWA

---

## 👤 Author

**Nishit Modi** 
