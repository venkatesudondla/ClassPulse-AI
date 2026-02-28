# ClassPulse-AI
# 🎓 ClassPulse-AI

ClassPulse-AI is an AI-powered classroom intelligence platform that analyzes live student video streams to measure engagement, attention levels, and emotional states in real time. The system provides actionable insights to educators through a dynamic dashboard, helping improve teaching effectiveness and learning outcomes.

The goal of this project is to transform traditional classrooms into data-driven, intelligent learning environments using computer vision and deep learning.

---

## 📌 Table of Contents

- [Overview](#overview)
- [Features](#features)
- [System Architecture](#system-architecture)
- [Tech Stack](#tech-stack)
- [Quick Start Guide](#quick-start-guide)
- [Environment Setup](#environment-setup)
- [Running the Application](#running-the-application)
- [AI Model & Engagement Scoring](#ai-model--engagement-scoring)
- [Project Structure](#project-structure)
- [Future Enhancements](#future-enhancements)
- [License](#license)

---

## 📖 Overview

ClassPulse-AI uses computer vision and deep learning to monitor classroom engagement in real time. By analyzing student facial expressions and attention patterns from video streams, the system generates engagement scores and emotion analytics.

The platform consists of:
- AI backend for video analysis
- Teacher dashboard for visualization
- Student interface for joining sessions

---

## 🚀 Features

- 🔴 Real-time video analysis using WebRTC
- 😊 Emotion detection (Happy, Neutral, Sad, Angry, Surprise, Fear, Disgust)
- 📊 Engagement score calculation (0% - 100%)
- 📈 Live teacher dashboard with analytics
- 📉 Post-session performance insights
- 🔐 Privacy-focused video handling
- ⚡ FastAPI-based scalable backend

---

## 🧠 System Architecture

```
Student Camera → WebRTC → AI Backend (FastAPI)
                     ↓
            Face Detection (OpenCV)
                     ↓
         Emotion Classification (ViT Model)
                     ↓
         Engagement Score Calculation
                     ↓
             Teacher Dashboard (React)
```

---

## 🛠 Tech Stack

| Layer | Technology |
|-------|------------|
| Backend | Python, FastAPI, Uvicorn |
| AI / ML | OpenCV, Hugging Face Vision Transformer (ViT), PyTorch |
| Frontend | React, Vite, Tailwind CSS |
| Streaming | WebRTC |
| Database | PostgreSQL (SQLAlchemy ORM) |
| API Communication | WebSockets |

---

## ⚡ Quick Start Guide

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/venkatesudondla/ClassPulse-AI.git
cd ClassPulse-AI
```

---

### 2️⃣ Backend Setup

```bash
cd backend

python -m venv venv
```

Activate virtual environment:

- Windows:
```bash
venv\Scripts\activate
```

- Mac/Linux:
```bash
source venv/bin/activate
```

Install dependencies:

```bash
pip install -r requirements.txt
```

Start backend server:

```bash
uvicorn app.main:app --reload --port 8000
```

---

### 3️⃣ Frontend Setup (Teacher Dashboard)

```bash
cd frontend/teacher-dashboard
npm install
npm run dev
```

Open:
```
http://localhost:5173
```

---

### 4️⃣ Frontend Setup (Student App)

```bash
cd frontend/student-app
npm install
npm run dev
```

Open:
```
http://localhost:3000
```

---

## 🔧 Environment Setup

Make sure the following are installed:

- Python 3.10+
- Node.js 18+
- PostgreSQL

Create a PostgreSQL database:

```
classpulse_ai
```

Set environment variable in backend:

```
DATABASE_URL=postgresql+asyncpg://postgres:password@localhost:5432/classpulse_ai
```

---

## 🤖 AI Model & Engagement Scoring

### Emotion Detection

The system uses a Hugging Face Vision Transformer (ViT) model to classify facial expressions into:

- Happy
- Neutral
- Sad
- Angry
- Surprise
- Fear
- Disgust

---

### Engagement Score Calculation

Engagement score is computed using weighted metrics:

- Face detected → +30%
- Eye focus / head orientation → +40%
- Emotion modifier → (-10% to +30%)

Final engagement score = (Face + Focus + Emotion Modifier)

Each student receives an individual score, and the classroom average is displayed on the dashboard.

---

## 📁 Project Structure

```
ClassPulse-AI/
│
├── backend/
│   ├── app/
│   ├── models/
│   └── requirements.txt
│
├── frontend/
│   ├── teacher-dashboard/
│   └── student-app/
│
├── database/
│
├── images/
│
├── README.md
└── .gitignore
```

---

## 📈 Future Enhancements

- 📱 Mobile application for teachers
- 📊 Advanced analytics dashboard
- 🧠 Attention tracking using gaze detection
- 📚 LMS integration (Moodle, Google Classroom)
- ☁️ Cloud deployment (AWS / Azure / GCP)
- 🔍 Personalized learning recommendations

---

## 📜 License

This project is open-source and available for educational and research purposes.
