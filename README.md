# AcneAI 

## Overview

AcneAI was developed as our Final Year Project (FYP) for the BS Computer Science program at the Punjab University College of Information Technology (PUCIT).

The goal of the project was to build an AI-powered web application that assists users in acne analysis using facial images. In addition to acne detection, the platform provides acne type classification, severity assessment, treatment recommendations, skincare product ingredient analysis, progress tracking, and an AI-powered dermatology assistant.
>
> AcneAI is intended for educational and informational purposes only. It does **not** replace professional medical advice, diagnosis, or treatment.

---
### My Role

I was responsible for the AI and backend development of the project.

### AI Development

I designed, trained, evaluated, and deployed the machine learning pipeline used by AcneAI. My work included:

- Collecting and preparing the training dataset
- Image preprocessing and augmentation
- Training three EfficientNet-B3 models for:
  - Acne Detection
  - Acne Type Classification
  - Acne Severity Classification
- Model evaluation and performance optimization
- Converting trained PyTorch models to ONNX for faster inference
- Integrating ONNX Runtime into the production backend

The final models achieved:

| Model | Accuracy |
|--------|----------|
| Acne Detection | **94%** |
| Acne Type Classification | **89%** |
| Severity Classification | **86%** |

### Backend Development

I designed and implemented the backend using FastAPI and integrated all AI services into a scalable web application.

Some of the major components I developed include:

- REST APIs using FastAPI
- JWT-based authentication and authorization
- Image upload and preprocessing pipeline
- Asynchronous ML inference using Celery and Redis
- PostgreSQL database design with Supabase
- Analysis history and progress tracking APIs
- Treatment recommendation engine
- Product ingredient scanner using Tesseract OCR and Groq LLM
- DermaAI chatbot backend and conversation management
- Cloudinary image storage
- Logging, API optimization, and production configuration

One of the primary challenges was deploying deep learning models efficiently on CPU-only cloud infrastructure. To address this, I converted the trained models to ONNX, integrated asynchronous inference using Celery workers, and designed a background job architecture that allows users to continue using the application while image analysis runs in parallel. This approach reduced response times and improved the overall user experience.

# Features

## AI Acne Detection

- Detect acne from facial images
- Identify acne type
- Assess severity level
- Fast ONNX inference

## Progress Tracking

- Store previous analyses
- Compare skin over time
- Monitor treatment effectiveness


##  Personalized Treatment Recommendations

Based on the detected:

- Acne type
- Severity level

AcneAI recommends

- Medicated treatments
- Herbal remedies
- Lifestyle improvements
- Dermatologist consultation when necessary

## Product Ingredient Scanner

Upload a skincare product label.

AcneAI automatically

- Extracts ingredients using OCR
- Detects comedogenic ingredients
- Suggests safer alternatives
- Calculates an overall suitability score

## DermaAI Assistant

An AI dermatologist assistant powered by an LLM that can answer questions related to

- Acne
- Skincare
- Ingredients
- Treatments
- Routines

## Authentication

- JWT Authentication
- Protected routes
- Secure password hashing
- User history

# Model Performance

| Task | Accuracy |
|------|----------|
| Acne Detection | **94%** |
| Acne Type Classification | **89%** |
| Severity Classification | **86%** |


---

# Tech Stack
**Frontend**: React, Vite, Tailwind CSS, React Router, Axios, Framer Motion, Lucide Icons

**Backend**: FastAPI, SQLAlchemy, Alembic, PostgreSQL, Supabase, JWT Authentication, Celery, Redis

**Machine Learning**: EfficientNet-B3, PyTorch, ONNX Runtime, OpenCV, NumPy, Pillow

**AI**: Groq LLM, Tesseract OCR

**Cloud**: Vercel, Cloudinary, Supabase, Upstash Redis

---

# Getting Started

## Clone the repository

```bash
git clone https://github.com/USERNAME/AcneAI.git
```

```
cd AcneAI
```

## Frontend

```bash
cd frontend
npm install
npm run dev
```


## Backend

```bash
cd backend

python -m venv .venv

source .venv/bin/activate
```

Windows

```bash
.venv\Scripts\activate
```

Install dependencies

```bash
pip install -r requirements.txt
```

Run FastAPI

```bash
uvicorn app.main:app --reload
```

## Environment Variables

Create a `.env` file inside the backend directory.

```
DATABASE_URL=

SUPABASE_URL=

SUPABASE_KEY=

REDIS_URL=

CLOUDINARY_URL=

GROQ_API_KEY=

JWT_SECRET=
```

---

# 🎥 Demo

```
https://drive.google.com/file/d/1UlRXijsR0nhDGarXGlVuL_22rU9NOMPi/view
```

---

# Future Work

- Mobile application
- Support additional skin diseases
- Clinical validation
- Better personalization
- Multilingual support
- Larger datasets
- Explainable AI (XAI)

---

# Authors

- **Areeba Khaliq**
- Aima Arfaq
- Uswa Farheen
- Urwa Amir

Department of Computer Science

Punjab University College of Information Technology (PUCIT)

University of the Punjab

---

# License

This project was developed as a Final Year Project at PUCIT and is intended for educational and research purposes.
