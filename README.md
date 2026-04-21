# MinorProject_CivicPulse_AnjaliBhadoriya
Minor Project I - Smart Civic Complaint Management System

# 🏛️ CivicPulse v2.0 — Production-Ready Smart Civic Complaint System

A fully-featured, production-grade smart city complaint management platform with AI detection, real-time notifications, analytics, role-based access, Docker support, CI/CD pipelines, and full test coverage.

---

## ⚡ Quick Start (Local Development)

### Prerequisites

| Tool    | Minimum Version  |
| ------- | ---------------- |
| Node.js | 18.x LTS         |
| npm     | 9.x              |
| MongoDB | 6.x or Atlas URI |

### Clone & Install

```bash
git clone <your-repo-url> civicpulse
cd civicpulse
npm run install:all
```

### Configure Environment

```bash
nano server/.env
```

### Seed Demo Data

```bash
npm run seed
```

### Start Development

```bash
npm run dev
```

| Service      | URL                              |
| ------------ | -------------------------------- |
| Frontend     | http://localhost:3000            |
| Backend API  | http://localhost:5000/api        |
| Health Check | http://localhost:5000/api/health |

---

## 🐳 Docker Setup

### Development

```bash
docker compose up -d
```

### Production

```bash
cp server/.env.example server/.env.production
docker compose -f docker-compose.prod.yml up -d
```

---

## 🔐 Demo Accounts

| Role    | Email                                       | Password |
| ------- | ------------------------------------------- | -------- |
| Admin   | [admin@demo.com](mailto:admin@demo.com)     | demo123  |
| Citizen | [citizen@demo.com](mailto:citizen@demo.com) | demo123  |
| Officer | [officer@demo.com](mailto:officer@demo.com) | demo123  |

Public dashboard available at:

```text
/public
```

---

## 📁 Project Structure

```text
civicpulse/
├── client/
├── server/
├── nginx/
├── .github/workflows/
├── docker-compose.yml
├── docker-compose.prod.yml
├── Makefile
└── README.md
```

---

## 🔌 API Reference

### Auth

| Method | Endpoint           |
| ------ | ------------------ |
| POST   | /api/auth/register |
| POST   | /api/auth/login    |
| GET    | /api/auth/me       |
| PUT    | /api/auth/profile  |

### Complaints

| Method | Endpoint                   |
| ------ | -------------------------- |
| POST   | /api/complaints            |
| GET    | /api/complaints/my         |
| GET    | /api/complaints/:id        |
| POST   | /api/complaints/:id/upvote |

### Admin

| Method | Endpoint                         |
| ------ | -------------------------------- |
| GET    | /api/admin/complaints            |
| PUT    | /api/admin/complaints/:id/status |
| PUT    | /api/admin/complaints/:id/assign |

### Public

| Method | Endpoint               |
| ------ | ---------------------- |
| GET    | /api/public/complaints |
| GET    | /api/public/stats      |

---

## 🧪 Running Tests

```bash
cd server
npm test
```

Coverage:

```bash
open coverage/lcov-report/index.html
```

---

## 🔒 Security Features

* bcrypt password hashing
* JWT authentication
* Helmet security headers
* Rate limiting
* XSS protection
* Mongo sanitize
* File validation
* Express validator

---

## 🌐 Production Deployment

```bash
docker compose -f docker-compose.prod.yml up -d
curl https://yourdomain.com/api/health
```

---

## 🛠️ Tech Stack

* React 18
* Node.js
* Express.js
* MongoDB
* Mongoose
* Socket.io
* Docker
* Nginx
* Jest
* GitHub Actions

---

## 🚨 Troubleshooting

### MongoDB not connecting?

```bash
mongosh --eval "db.adminCommand('ping')"
```

### Port already in use?

```bash
PORT=5001
```

### JWT expired?

```env
JWT_EXPIRE=30d
```

---

## 📄 License

MIT © CivicPulse 2024


