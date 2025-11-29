# AgroFund 🌱💼

Revolutionizing agricultural investment with AI-powered risk assessment, direct farmer–investor matching, and a built-in job marketplace.

## Table of Contents

- [Project Overview](#project-overview)
- [Features](#features)
  - [For Farmers](#for-farmers)
  - [For Investors](#for-investors)
  - [For Workers](#for-workers)
- [Technology Stack](#technology-stack)
- [Quick Start](#quick-start)
- [Detailed Installation Guide](#detailed-installation-guide)
  - [Backend Setup](#backend-setup)
  - [Frontend Setup](#frontend-setup)
  - [AI Integration Setup](#ai-integration-setup)
- [API Documentation](#api-documentation)
- [Database Schema](#database-schema)
- [Environment Variables](#environment-variables)
- [Deployment](#deployment)
- [Troubleshooting](#troubleshooting)
- [Support](#support)
- [License](#license)
- [Acknowledgments](#acknowledgments)

## Project Overview

AgroFund is an intelligent platform that connects investors with farming projects through AI-powered risk assessment. Farmers can showcase their projects, investors discover vetted opportunities, and agricultural workers find jobs — all in one seamless ecosystem.

**Key Value Propositions**

🤖 AI-driven risk assessment  
👨‍🌾 Direct farmer–investor matching  
💼 Job posting & application system  
💬 Smart farming assistant chatbot  
📊 Real-time project analytics dashboard

## Features

### For Farmers
- Create and manage agricultural projects
- Get AI-powered risk scoring
- Post job opportunities
- Connect directly with investors
- Use the smart farming assistant

### For Investors
- Browse vetted agricultural projects
- View AI-generated risk analysis & scores
- Submit investment requests
- Portfolio management dashboard
- Direct messaging with farmers

### For Workers
- Browse farm job postings
- Apply with one click
- Manage profile & applications
- Track application status

## Technology Stack

**Backend**  
Node.js • Express.js • Prisma ORM • PostgreSQL (Neon) • JWT + bcrypt

**Frontend**  
Next.js • Context API / Redux • Axios • Modern CSS (Tailwind/Shadcn/etc.)

**AI Integration**  
FastAPI (Python) • scikit-learn • Joblib • Uvicorn

**Infrastructure**  
Neon.tech • GitHub • Postman • Nginx (production)

## Quick Start

```bash
# Clone the repository
git clone https://github.com/AgroFund-Algeria2-0/agroFundRep.git
cd agrofund

cd agrroConnect

# Backend
cd backend
npm install
cp .env.example .env   
npx prisma db push
npm run dev             

# Frontend (new terminal)

npm install
cp .env.example .env   # edit .env
npm start               # runs on http://localhost:3000

# AI Service (new terminal)
cd ../riskEstimation_
python -m venv venv
# Windows
venv\Scripts\activate
# macOS/Linux
# source venv/bin/activate
pip install -r requirements.txt
uvicorn app.minimal_main:app --reload --port 8000

Detailed Installation Guide
Backend Setup
Prerequisites: Node.js ≥16, PostgreSQL (Neon recommended
cd backend
npm install
cp .env.example .env
# Edit .env → add DATABASE_URL, JWT_SECRET, etc.

npx prisma generate
npx prisma db push
npm run dev

Backend runs on http://localhost:3000
cd frontend
npm install
cp .env.example .env

npm start

AI Integration Setup
Prerequisites: Python ≥3.8
Bashcd ai-integration
python -m venv venv
# Activate venv (see Quick Start)
pip install -r requirements.txt
uvicorn app.minimal_main:app --reload --host 0.0.0.0 --port 8000
→ AI service runs on http://localhost:8000
Main AI endpoint
POST http://localhost:8000/predict → returns risk score + analysis
API Documentation
Full interactive documentation & collection:
https://documenter.getpostman.com/view/47276242/2sB3dLTBaL

DATABASE_URL="postgresql://..."
JWT_SECRET="your-super-secret-jwt-key"
JWT_EXPIRES_IN="7d"

PORT=3000
NODE_ENV="development"

# Backend (production)
cd backend
npm run build        # if using TypeScript/babel
NODE_ENV=production npm start

# Frontend (production)
cd frontend
npm run build      


Troubleshooting

Database connection → check DATABASE_URL and Neon IP whitelist
CORS errors → verify allowed origins in backend
AI model not loading → confirm model path & Python requirements
JWT issues → ensure same JWT_SECRET and token not expired


License
MIT License (or your preferred license)

Acknowledgments
Immense gratitude to farmers, agronomists, investment experts, and the open-source community.
AgroFund — Cultivating Growth, Harvesting Success 🌾
