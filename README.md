# 📧 AI Corporate Email Generator

A full-stack GenAI application that converts simple user instructions into professional corporate emails using modern LLM architecture.

This project demonstrates:

* ✅ Prompt Engineering
* ✅ LCEL (LangChain Expression Language)
* ✅ FastAPI Backend
* ✅ Streamlit Frontend
* ✅ LLMOps with LangSmith
* ✅ Production Deployment (Render + Streamlit Cloud)

---

## 🚀 Live Demo

* 🔹 **Frontend**: [https://corporate-mail-frontend-by-bala.streamlit.app](https://corporate-mail-frontend-by-bala.streamlit.app)
* 🔹 **Backend API Docs**: [https://corporate-mail-backend.onrender.com/docs](https://corporate-mail-backend.onrender.com/docs)

---

# 🏗 Architecture

```
User
  ↓
Streamlit (Frontend)
  ↓
FastAPI (Backend)
  ↓
Groq LLM (Generation)
  ↓
LangSmith (Tracing & Evaluation)
```

---

# 🧠 Features

## ✨ Email Generation Controls

* Tone (Polite / Neutral / Escalation)
* Email Type (Request / Follow-up / Status Update, etc.)
* Length (Short / Medium / Detailed)
* Formality Level
* Audience Selection
* Urgency Level
* Language Style
* Call-to-Action toggle
* Signature Style

---

## ⚙ Backend Features

* Async FastAPI endpoints
* LCEL-based LLM pipeline
* Environment variable management
* CORS configuration
* Health check endpoint
* Structured request validation (Pydantic v2)
* Production-ready deployment

---

## 📊 LLMOps & Evaluation

This project includes:

* LangSmith tracing
* LLM-as-Judge evaluator
* Numeric scoring (1–5)
* Quality monitoring
* Prompt versioning capability
* Evaluation insights dashboard

---

# 🧩 Tech Stack

## Backend

* FastAPI
* Uvicorn
* LangChain (LCEL)
* Groq LLM
* LangSmith
* Pydantic v2

## Frontend

* Streamlit
* Requests

## Deployment

* Render (Backend)
* Streamlit Community Cloud (Frontend)

---

# 🔧 Installation (Local Development)

## 1️⃣ Clone the repo

```bash
git clone https://github.com/Balusanu/Corporate-mail-generator-app
cd Corporate-mail-generator-app
```

---

## 2️⃣ Create virtual environment

```bash
python -m venv venv
source venv/bin/activate  # Mac/Linux
venv\Scripts\activate     # Windows
```

---

## 3️⃣ Install dependencies

```bash
pip install -r requirements.txt
```

---

## 4️⃣ Set environment variables

Create `.env` (DO NOT commit this file):

```
GROQ_API_KEY=your_key_here
LANGCHAIN_API_KEY=your_langsmith_key
LANGCHAIN_TRACING_V2=true
LANGCHAIN_PROJECT=email-generator
```

---

## 5️⃣ Run Backend

```bash
uvicorn main:app --reload
```

Open:

```
http://127.0.0.1:8000/docs
```

---

## 6️⃣ Run Frontend

```bash
streamlit run app.py
```

---

# 🧠 LCEL Pipeline

The email generation pipeline uses modern LangChain Expression Language:

```python
chain = email_prompt | llm | StrOutputParser()
```

This enables:

* Modular composition
* Async execution
* Easy model switching
* Better tracing in LangSmith

---

# 🔐 Security Practices

* No API keys stored in GitHub
* Environment variables used in production
* CORS restricted to frontend domain
* Fail-fast environment validation

---

# 📈 LLMOps Strategy

The system uses:

* Prompt versioning
* LLM-as-Judge scoring
* Numeric evaluation metrics
* Composite scoring capability
* Production trace monitoring

This enables continuous improvement and regression detection.

---

# 📌 Author

**Balasubramanya C K**
AI / Data Enthusiast | GenAI Builder | Automation Specialist