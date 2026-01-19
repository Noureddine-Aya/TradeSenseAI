# 📈 TradeSense AI - Prop Trading Platform

<div align="center">

![TradeSense AI](https://img.shields.io/badge/TradeSense-AI-6366f1?style=for-the-badge&logo=chart-line)
![Python](https://img.shields.io/badge/Python-3.10+-3776AB?style=flat-square&logo=python)
![React](https://img.shields.io/badge/React-19-61DAFB?style=flat-square&logo=react)
![Flask](https://img.shields.io/badge/Flask-3.0-000000?style=flat-square&logo=flask)

**🌍 La Première Prop Firm Assistée par IA pour l'Afrique**

[✨ Features](#-features) • [🚀 Installation](#-installation) • [📡 API](#-api-endpoints) • [🎮 Usage](#-usage-guide)

</div>

---

## 🎯 About

**TradeSense AI** est une plateforme SaaS de **Prop Trading** permettant aux utilisateurs de :

- 💳 Participer à des challenges de trading (Starter, Pro, Elite)
- 📊 Trader avec du capital virtuel basé sur des données de marché
- ⚖️ Être évalués selon des règles strictes (drawdown & profit target)
- 🏆 Devenir traders **Funded** après réussite du challenge

---

## ✨ Features

| Module | Description |
|------|-------------|
| 🏆 **Challenge Engine** | Balances virtuelles (5K$–50K$), règles (5% perte journalière, 10% perte totale, 10% objectif) |
| 💳 **Payments** | Paiements mock (CMI, Crypto) + PayPal (admin) |
| 📊 **Dashboard** | Charts TradingView, prix temps réel, signaux IA |
| 🏅 **Leaderboard** | Top 10 traders, statistiques globales |
| 👤 **Auth** | Authentification JWT |
| 🔧 **Admin Panel** | Gestion utilisateurs, challenges et paiements |

---

## 🚀 Installation

### Prérequis

- Python 3.10+
- Node.js 20+
- npm ou yarn

### 1️⃣ Cloner le dépôt

```bash
git clone https://github.com/yourusername/tradesense-ai.git
cd tradesense-ai
````

### 2️⃣ Backend (Flask)

```bash
cd backend

python -m venv venv
venv\Scripts\activate    # Windows
# source venv/bin/activate  # Linux / Mac

pip install -r requirements.txt
copy .env.example .env

python app.py
```

➡ Backend : `http://localhost:5000`

---

### 3️⃣ Frontend (React + Vite)

```bash
cd frontend
npm install
npm run dev
```

➡ Frontend : `http://localhost:5173`

---

## 📁 Structure du Projet

```text
tradesense-ai/
├── backend/
│   ├── app.py
│   ├── config.py
│   ├── models.py
│   ├── requirements.txt
│   ├── routes/
│   │   ├── auth.py
│   │   ├── challenge.py
│   │   ├── trades.py
│   │   ├── payments.py
│   │   ├── market.py
│   │   ├── leaderboard.py
│   │   └── admin.py
│   └── services/
│       ├── challenge_engine.py
│       ├── market_data.py
│       └── ai_signals.py
│
├── frontend/
│   └── src/
│       ├── App.jsx
│       ├── index.css
│       ├── components/
│       └── pages/
│
└── database.sql
```

---

## ⚙️ Variables d'Environnement

Créer `backend/.env` :

```env
SECRET_KEY=your-secret-key
FLASK_ENV=development
DATABASE_URL=sqlite:///tradesense.db
JWT_SECRET_KEY=your-jwt-secret
CORS_ORIGINS=http://localhost:5173,http://localhost:3000
```

---

## 📡 API Endpoints

### 🔐 Authentication

| Method | Endpoint           |
| ------ | ------------------ |
| POST   | /api/auth/register |
| POST   | /api/auth/login    |
| GET    | /api/auth/me       |

### 🏆 Challenges

| Method | Endpoint               |
| ------ | ---------------------- |
| GET    | /api/challenges        |
| GET    | /api/challenges/active |
| GET    | /api/challenges/plans  |

### 💹 Trading

| Method | Endpoint              |
| ------ | --------------------- |
| POST   | /api/trades           |
| GET    | /api/trades           |
| GET    | /api/trades/positions |

### 📊 Market

| Method | Endpoint            |
| ------ | ------------------- |
| GET    | /api/market/prices  |
| GET    | /api/market/signals |

### 💳 Payments

| Method | Endpoint               |
| ------ | ---------------------- |
| GET    | /api/payments/plans    |
| POST   | /api/payments/checkout |

### 🏅 Leaderboard

| Method | Endpoint               |
| ------ | ---------------------- |
| GET    | /api/leaderboard       |
| GET    | /api/leaderboard/stats |

---

## 🎮 Usage Guide

1️⃣ Inscription → `/auth`
2️⃣ Acheter un challenge → `/pricing`
3️⃣ Trader → `/dashboard`
4️⃣ Réussir le challenge → +10% profit sans dépasser le drawdown

---

## 🛠️ Tech Stack

| Layer    | Tech                   |
| -------- | ---------------------- |
| Backend  | Flask, SQLAlchemy, JWT |
| Frontend | React 19, Vite         |
| DB       | SQLite / PostgreSQL    |
| Charts   | TradingView            |
| Data     | Yahoo Finance          |
| UI       | Dark Theme Custom      |

---

## 🚢 Déploiement

---

## 🚀 Deployment

### Backend (Render)

1. **Build command**: `pip install -r requirements.txt`
2. **Start command**: `gunicorn app:app`
3. **Environment Variables**:
   - `DATABASE_URL`: Your PostgreSQL URL (or use default SQLite)
   - `SECRET_KEY`: A strong random string
   - `JWT_SECRET_KEY`: Another strong random string
   - `CORS_ORIGINS`: `https://your-app-name.vercel.app` (Your Vercel URL)

### Frontend (Vercel)

1. **Framework Preset**: `Vite`
2. **Root Directory**: `frontend`
3. **Environment Variables**:
   - `VITE_API_URL`: `https://tradesenseai-g09w.onrender.com/api`

---

## 🤝 Contributing

1. Fork
2. Branch feature
3. Commit
4. Push
5. Pull Request

---

## 📄 License

MIT License

---

<div align="center">

**Construit avec ❤️ pour la communauté de trading africaine**

[⬆ Retour en haut](#-tradesense-ai---prop-trading-platform)

</div>

