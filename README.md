# AcneAI 

## Overview

AcneAI was developed as our Final Year Project (FYP) for the BS Computer Science program at the Punjab University College of Information Technology (PUCIT).

The goal of the project was to build an AI-powered web application that assists users in acne analysis using facial images. In addition to acne detection, the platform provides acne type classification, severity assessment, treatment recommendations, skincare product ingredient analysis, progress tracking, and an AI-powered dermatology assistant.
>
> AcneAI is intended for educational and informational purposes only. It does **not** replace professional medical advice, diagnosis, or treatment.

---
### My Role

I led the AI and backend development of AcneAI.

On the AI side, I built the complete machine learning pipeline by preparing the dataset, training and evaluating three EfficientNet-B3 models for acne detection, acne type classification, and severity assessment, and optimizing them for deployment using ONNX Runtime.

On the backend, I developed the FastAPI application, integrated the trained models into an asynchronous inference pipeline using Celery and Redis, designed the PostgreSQL database with Supabase, implemented authentication and core APIs, and integrated the DermaAI chatbot and OCR-based product ingredient scanner.

This work resulted in a scalable cloud-based application capable of performing end-to-end acne analysis.

The final models achieved:

| Model | Accuracy |
|--------|----------|
| Acne Detection | **94%** |
| Acne Type Classification | **89%** |
| Severity Classification | **86%** |

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
