# EduPulse AI — AI-Powered Early Detection of Student Academic Disengagement

> **Early insights. Timely support. Better learning.**

EduPulse AI is a full-stack educational technology application designed to help faculty identify early patterns that may indicate a student needs academic support.

The system combines academic and engagement indicators such as attendance, assignment completion, assessment performance, learning activity, and participation trends. It uses machine learning to generate an early engagement indicator, provides understandable explanations of the factors associated with the model output, and enables faculty to review alerts and record appropriate academic support.

---

## Table of Contents

- [1. Project Overview](#1-project-overview)
- [2. Problem Statement](#2-problem-statement)
- [3. Objectives](#3-objectives)
- [4. Key Features](#4-key-features)
- [5. System Workflow](#5-system-workflow)
- [6. Technology Stack](#6-technology-stack)
- [7. Project Architecture](#7-project-architecture)
- [8. Application Modules](#8-application-modules)
- [9. AI/ML Pipeline](#9-aiml-pipeline)
- [10. Explainable AI](#10-explainable-ai)
- [11. Early Alert and Support Workflow](#11-early-alert-and-support-workflow)
- [12. Privacy and Responsible AI](#12-privacy-and-responsible-ai)
- [13. Project Structure](#13-project-structure)
- [14. Local Installation](#14-local-installation)
- [15. Environment Variables](#15-environment-variables)
- [16. Running the Application](#16-running-the-application)
- [17. Dataset](#17-dataset)
- [18. Model Evaluation](#18-model-evaluation)
- [19. Testing](#19-testing)
- [20. Deployment](#20-deployment)
- [21. Demo Flow](#21-demo-flow)
- [22. Limitations](#22-limitations)
- [23. Future Enhancements](#23-future-enhancements)
- [24. Team](#24-team)
- [25. License](#25-license)

---

# 1. Project Overview

EduPulse AI is designed as a decision-support platform for faculty and academic mentors.

Instead of looking at attendance, assignments, assessments, and learning activity separately, the application brings these indicators together and analyses their patterns over time.

The system can:

1. Collect and validate academic and engagement data.
2. Display student-level and class-level trends.
3. Process relevant features for machine learning.
4. Generate an early engagement indicator when an appropriate trained model is available.
5. Explain the indicators associated with the model output.
6. Generate reviewable early alerts.
7. Provide possible academic support options.
8. Record faculty review and follow-up actions.
9. Protect student information through authentication and role-based access.

**Important:** EduPulse AI is a decision-support system. An AI output is not a diagnosis, definitive judgment, or automatic disciplinary decision. Faculty review is required before intervention.

---

# 2. Problem Statement

Academic disengagement can develop gradually. Changes in attendance, assignment completion, assessment performance, participation, and learning activity may appear before a student experiences a significant academic setback.

However, these indicators are often stored or reviewed separately.

EduPulse AI addresses this problem by creating a unified platform that analyses relevant academic and engagement indicators, identifies meaningful changes and patterns, provides explainable AI insights, and alerts authorized faculty when a situation may require attention.

The intended outcome is earlier, more informed and supportive academic intervention.

---

# 3. Objectives

### Primary objectives

- Identify meaningful changes in student engagement indicators.
- Analyse attendance, assignments, assessments and learning activity together.
- Apply machine learning when suitable labelled data is available.
- Provide understandable explanations for model outputs.
- Display student-level and class-level engagement trends.
- Generate early alerts for authorized faculty.
- Provide possible academic support options.
- Maintain a faculty review and follow-up workflow.
- Protect student privacy and restrict access to authorized users.

### Responsible AI objective

The system is designed to assist faculty rather than replace human judgment.

---

# 4. Key Features

## Student and academic analytics

- Attendance trends
- Assignment completion trends
- Assessment performance
- Learning activity
- Participation trends
- Historical engagement changes
- Student-level analytics
- Class-level analytics
- Search, filtering and reporting periods

## AI/ML

- Data preprocessing and validation
- Feature engineering
- Classification-based early engagement indicator
- Model evaluation
- Prediction API
- Feature importance / explanation
- Model limitation reporting

## Early alerts

- Reviewable academic alerts
- Alert status
- Alert date and reporting period
- Supporting indicators
- Duplicate-alert prevention
- Faculty review workflow

## Academic support

Possible support options include:

- Academic mentoring
- Assignment guidance
- Study-planning assistance
- Faculty consultation
- Follow-up review

## Security

- Authentication
- Role-based authorization
- Protected API routes
- Password hashing
- Environment-based secrets
- Upload validation
- Audit trail for important actions

## User experience

- Responsive design
- Student-friendly interface
- Faculty dashboard
- Interactive charts
- Loading and error states
- Accessible navigation
- Mobile, tablet and desktop support

---

# 5. System Workflow

```text
                 ┌──────────────────────┐
                 │ Academic Data        │
                 │ Attendance           │
                 │ Assignments          │
                 │ Assessments          │
                 │ Learning Activity   │
                 └──────────┬───────────┘
                            │
                            ▼
                 ┌──────────────────────┐
                 │ Data Validation &    │
                 │ Preprocessing        │
                 └──────────┬───────────┘
                            │
                            ▼
                 ┌──────────────────────┐
                 │ Feature Engineering  │
                 └──────────┬───────────┘
                            │
                            ▼
                 ┌──────────────────────┐
                 │ AI / ML Model        │
                 │ Classification       │
                 └──────────┬───────────┘
                            │
                            ▼
                 ┌──────────────────────┐
                 │ Explainable AI       │
                 │ Contributing         │
                 │ Indicators           │
                 └──────────┬───────────┘
                            │
                            ▼
                 ┌──────────────────────┐
                 │ Early Alert          │
                 └──────────┬───────────┘
                            │
                            ▼
                 ┌──────────────────────┐
                 │ Faculty Review       │
                 └──────────┬───────────┘
                            │
                            ▼
                 ┌──────────────────────┐
                 │ Academic Support     │
                 └──────────┬───────────┘
                            │
                            ▼
                 ┌──────────────────────┐
                 │ Follow-up &          │
                 │ Monitoring           │
                 └──────────────────────┘
```

---

# 6. Technology Stack

| Layer | Technology |
|---|---|
| Frontend | React + Vite |
| Styling | Tailwind CSS |
| Animation | Framer Motion |
| Charts | Recharts |
| Backend | Python + FastAPI |
| Data processing | Pandas + NumPy |
| Machine Learning | Scikit-learn |
| Database | PostgreSQL |
| Local database | SQLite |
| Authentication | Secure server-side authentication |
| API | REST |
| Version control | Git + GitHub |
| Frontend deployment | Vercel or equivalent |
| Backend deployment | Render or equivalent |

---

# 7. Project Architecture

```text
                         ┌─────────────────┐
                         │   React Client  │
                         │  Web Interface  │
                         └────────┬────────┘
                                  │ REST API
                                  ▼
                         ┌─────────────────┐
                         │   FastAPI       │
                         │   Backend       │
                         └───────┬─────────┘
                                 │
             ┌───────────────────┼───────────────────┐
             │                   │                   │
             ▼                   ▼                   ▼
      ┌────────────┐      ┌─────────────┐     ┌──────────────┐
      │ PostgreSQL │      │ ML Pipeline │     │ Auth / RBAC  │
      │ Database   │      │             │     │              │
      └────────────┘      └──────┬──────┘     └──────────────┘
                                  │
                                  ▼
                         ┌─────────────────┐
                         │ Prediction +    │
                         │ Explainability  │
                         └────────┬────────┘
                                  │
                                  ▼
                         ┌─────────────────┐
                         │ Alerts &        │
                         │ Support         │
                         └─────────────────┘
```

---

# 8. Application Modules

## 8.1 Landing Page

The landing page introduces:

- EduPulse AI
- Project objective
- Key features
- How the system works
- Responsible AI principles
- Login access

## 8.2 Authentication

Users are authenticated according to their role.

Suggested roles:

- Administrator
- Faculty / Mentor
- Student

Access to student records is restricted according to authorization.

## 8.3 Faculty Dashboard

The dashboard provides:

- Student overview
- Attendance summary
- Assignment completion
- Assessment trends
- Engagement trends
- Recent alerts
- Class filters
- Date/reporting-period filters

## 8.4 Student Analytics

Faculty can view authorized academic information and historical trends.

## 8.5 AI Prediction

The AI module processes appropriate features and provides an engagement indicator when a validated model is available.

## 8.6 Explainable AI

The system displays the indicators associated with the prediction so faculty can understand why an alert may have been generated.

## 8.7 Early Alert Centre

Faculty can:

- View alerts
- Filter alerts
- Review supporting data
- Change alert status
- Record follow-up actions

## 8.8 Academic Support

The platform can display possible support options such as mentoring, assignment guidance and faculty consultation.

---

# 9. AI/ML Pipeline

The intended ML pipeline is:

```text
Raw Data
   ↓
Data Validation
   ↓
Missing Value Handling
   ↓
Feature Engineering
   ↓
Train/Test Split
   ↓
Model Training
   ↓
Model Evaluation
   ↓
Model Persistence
   ↓
Prediction API
   ↓
Explainable Output
```

## Input features

Potential features include:

- `attendance_percentage`
- `assignment_completion_percentage`
- `assessment_score`
- `learning_activity`
- `participation`
- Historical changes in these indicators

## Candidate models

The project can evaluate:

- Random Forest Classifier
- Logistic Regression
- Decision Tree

The final model should be selected based on actual validation results and project requirements rather than an assumed result.

## Important data rule

The application must not fabricate model accuracy.

If an appropriate labelled dataset is unavailable, the prototype should clearly identify its demonstration outputs as illustrative rather than presenting them as validated real-world predictions.

---

# 10. Explainable AI

EduPulse AI aims to make model outputs understandable.

For an individual prediction, the interface can show:

```text
AI Engagement Indicator

Attention may be required

Contributing indicators:
• Attendance trend
• Assignment completion trend
• Learning activity trend

Reporting period:
Current academic period

Action:
Faculty review recommended
```

The explanation should describe associations or model contributions, not claim that an indicator is definitely the cause of a student's academic situation.

---

# 11. Early Alert and Support Workflow

```text
AI / Trend Analysis
        ↓
Potential Concern
        ↓
Early Alert Created
        ↓
Faculty Reviews Evidence
        ↓
Faculty Records Decision
        ↓
Support Action
        ↓
Follow-up
        ↓
Monitor New Data
```

The system should not automatically punish, exclude, rank, or otherwise make high-impact decisions about students.

---

# 12. Privacy and Responsible AI

Student academic information can be sensitive. The project therefore follows these principles:

- Use synthetic or appropriately anonymized data for demonstrations.
- Restrict student records using role-based authorization.
- Do not expose private information in logs.
- Store secrets in environment variables.
- Validate uploaded files.
- Protect API endpoints.
- Use secure authentication.
- Require human review before intervention.
- Do not use AI output as a definitive judgment.
- Document model limitations.
- Avoid unsupported inferences from student data.
- Collect only information needed for the stated purpose.

---

# 13. Project Structure

A recommended project structure is:

```text
edupulse-ai/
│
├── frontend/
│   ├── src/
│   │   ├── components/
│   │   ├── pages/
│   │   ├── layouts/
│   │   ├── services/
│   │   ├── hooks/
│   │   ├── utils/
│   │   └── App.jsx
│   ├── public/
│   ├── package.json
│   └── vite.config.js
│
├── backend/
│   ├── app/
│   │   ├── api/
│   │   ├── models/
│   │   ├── schemas/
│   │   ├── services/
│   │   ├── ml/
│   │   ├── auth/
│   │   └── main.py
│   │
│   ├── tests/
│   ├── requirements.txt
│   └── .env.example
│
├── data/
│   ├── sample/
│   └── README.md
│
├── models/
│   └── README.md
│
├── docs/
│   ├── architecture.md
│   └── model-card.md
│
├── .gitignore
└── README.md
```

---

# 14. Local Installation

## Prerequisites

Install:

- Python 3.10+
- Node.js 18+
- npm
- Git

Verify:

```bash
python --version
node --version
npm --version
git --version
```

---

## Clone the project

```bash
git clone YOUR_GITHUB_REPOSITORY_URL
cd edupulse-ai
```

---

# 15. Environment Variables

Create the backend environment file from the example:

```bash
cp backend/.env.example backend/.env
```

On Windows, you can create the file manually if `cp` is unavailable.

Example:

```env
APP_ENV=development
SECRET_KEY=change-this-in-development
DATABASE_URL=sqlite:///./edupulse.db
CORS_ORIGINS=http://localhost:5173
```

For production, use secure secret values and a PostgreSQL connection string supplied by the hosting provider.

**Never commit `.env` to GitHub.**

---

# 16. Running the Application

## Backend

Create and activate a virtual environment:

### Windows

```powershell
python -m venv .venv
.venv\Scripts\activate
```

### macOS/Linux

```bash
python3 -m venv .venv
source .venv/bin/activate
```

Install dependencies:

```bash
cd backend
pip install -r requirements.txt
```

Start FastAPI:

```bash
uvicorn app.main:app --reload
```

The API will normally be available at:

```text
http://127.0.0.1:8000
```

FastAPI documentation is normally available at:

```text
http://127.0.0.1:8000/docs
```

---

## Frontend

Open another terminal:

```bash
cd frontend
npm install
npm run dev
```

The frontend will normally be available at:

```text
http://localhost:5173
```

---

# 17. Dataset

The demonstration version should use synthetic or appropriately anonymized academic data.

Example structure:

```csv
student_id,attendance_percentage,assignment_completion_percentage,assessment_score,learning_activity,participation
STU001,92,95,87,90,88
STU002,78,72,75,68,70
STU003,61,55,64,52,50
STU004,88,91,84,86,85
```

These values are examples only.

They must not be presented as real student records.

A production system should use an appropriately governed dataset and documented data permissions.

---

# 18. Model Evaluation

The model should be evaluated using an appropriate held-out test set.

Recommended metrics:

- Accuracy
- Precision
- Recall
- F1-score
- Confusion matrix

Example evaluation format:

```text
Model Evaluation
-----------------
Model: Random Forest

Accuracy: [actual result]
Precision: [actual result]
Recall: [actual result]
F1-score: [actual result]
```

Only replace the placeholders with results actually obtained from the trained and evaluated model.

For this project, the team should pay particular attention to false negatives and false positives because both can affect how faculty interpret alerts.

---

# 19. Testing

Run backend tests:

```bash
pytest
```

Run frontend checks:

```bash
npm run build
```

The final project should test:

- Authentication
- Role-based access
- Data validation
- CSV upload
- Database operations
- ML preprocessing
- ML prediction
- API responses
- Alert generation
- Duplicate-alert prevention
- Faculty follow-up
- Responsive UI
- Error states

---

# 20. Deployment

A possible production architecture is:

```text
                 Internet
                    │
                    ▼
          ┌───────────────────┐
          │ Frontend Hosting  │
          │ React + Vite      │
          └─────────┬─────────┘
                    │
                    │ HTTPS / REST
                    ▼
          ┌───────────────────┐
          │ Backend Hosting   │
          │ FastAPI           │
          └───────┬─────┬─────┘
                  │     │
                  ▼     ▼
           PostgreSQL   ML Model
```

Possible hosting services:

- Frontend: Vercel or equivalent
- Backend: Render or equivalent
- Database: Managed PostgreSQL

Before deployment:

```text
[ ] Remove secrets from source code
[ ] Remove real student data
[ ] Configure production environment variables
[ ] Configure CORS
[ ] Configure PostgreSQL
[ ] Build frontend
[ ] Test backend health endpoint
[ ] Test authentication
[ ] Test ML inference
[ ] Test database persistence
[ ] Test live application
```

---

# 21. Demo Flow

For a project presentation, use this sequence:

### 1. Landing Page

Explain the problem and objective.

### 2. Faculty Login

Demonstrate secure role-based access.

### 3. Dashboard

Show overall engagement indicators.

### 4. Student Analytics

Select a fictional student and show historical trends.

### 5. AI Prediction

Show the model output and contributing indicators.

### 6. Explainable AI

Explain why the output requires faculty attention.

### 7. Early Alert

Show how the alert reaches the faculty workflow.

### 8. Academic Support

Show possible support options.

### 9. Follow-up

Record the support action and monitoring status.

### 10. Privacy

Briefly demonstrate the access-control and responsible-AI approach.

---

# 22. Limitations

The prototype may have the following limitations:

1. Model performance depends on the quality and representativeness of the training data.
2. A validated predictive model requires suitable labelled historical data.
3. Synthetic demonstration data cannot establish real-world predictive performance.
4. Academic disengagement can have many causes that may not be represented in academic data.
5. Model outputs should not be interpreted as definitive judgments.
6. Faculty review remains necessary before intervention.
7. Production deployment requires appropriate institutional privacy, security and governance controls.

---

# 23. Future Enhancements

Possible future improvements include:

- Longitudinal time-series modelling
- More advanced explainability
- Personalized student dashboards
- LMS integration
- Attendance-system integration
- Automated reporting for authorized faculty
- Multilingual student support
- Mobile application
- Institution-wide analytics
- Model monitoring and drift detection
- Fairness and subgroup performance monitoring
- Improved intervention outcome tracking

---

# 24. Team

**Project:** EduPulse AI

**Title:** AI-Powered Early Detection of Student Academic Disengagement

**Team Members:**

- Member 1 — [Name]
- Member 2 — [Name]
- Member 3 — [Name]
- Member 4 — [Name]

**Institution:** [College / University Name]

**Department:** [Department Name]

**Event / Hackathon:** [Event Name]

---

# 25. License

This project is developed for educational and demonstration purposes.

If this project is deployed with real student information, appropriate institutional authorization, privacy controls, security practices, data governance, and applicable legal requirements must be established before use.

---

## Project tagline

> **EduPulse AI — Detect early. Understand clearly. Support better.**

---

## Acknowledgement

EduPulse AI is designed as an educational technology prototype demonstrating how academic analytics, machine learning, explainable AI, early alerts, and faculty support workflows can be combined into a responsible student-support platform.
