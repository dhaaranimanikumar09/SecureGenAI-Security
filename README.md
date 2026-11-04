# SecureGenAI-Security
A secure local GenAI chatbot built with Python, Streamlit, Ollama, and Llama 3.2, featuring prompt injection detection, PII protection, and role-based access control, with a proposed context-aware adaptive AI security framework.

# 🔐 SecureGenAI
### Context-Aware Security Framework for Generative AI Applications

**SecureGenAI** is a security-focused Generative AI chatbot designed to identify and mitigate security risks associated with Large Language Models (LLMs).

The project integrates local AI inference with prompt injection detection, Personally Identifiable Information (PII) protection, and role-based access checks.

Its proposed extension introduces an **Adaptive AI Security Engine** that evaluates multiple security signals and dynamically determines how potentially risky requests should be handled.

---

## 💡 Proposed Innovation

Traditional chatbot security implementations often rely on predefined rules and keyword-based filtering.

SecureGenAI aims to extend this approach through a **Context-Aware Adaptive Security Framework**.

The proposed framework will:

- Evaluate incoming prompts using multiple security signals.
- Calculate risk scores for potentially malicious requests.
- Identify prompt injection attempts.
- Detect and anonymize sensitive personal information.
- Evaluate user access permissions.
- Dynamically select appropriate security responses.
- Explain why a request was allowed, sanitized, restricted, or blocked.
- Extend security analysis to uploaded documents containing indirect prompt injection instructions.

**Core idea:** Move beyond simple prompt filtering towards adaptive, risk-based security for Generative AI applications.

---

## 🏗️ System Architecture

```text
              User Input
                  |
                  v
          Streamlit Interface
                  |
                  v
          Security Engine
                  |
        +---------+----------+
        |         |          |
        v         v          v
     Prompt     PII       Role-Based
   Detection  Detection    Access Check
        |         |          |
        +---------+----------+
                  |
                  v
          Local LLM Processing
                  |
                  v
           Ollama + Llama 3.2
                  |
                  v
          Output Validation
                  |
                  v
          Secure AI Response
```

*Adaptive risk scoring and document-context inspection are planned extensions.*

---

## 🛠️ Technology Stack

| Technology | Purpose |
|---|---|
| Python | Backend development |
| Streamlit | Chatbot interface |
| Ollama | Local AI model execution |
| Llama 3.2 | Large Language Model |
| LangChain | LLM integration |
| Microsoft Presidio | PII detection and anonymization |
| Regular Expressions | Basic prompt injection detection |
| Python Logging | Security event logging |
| Git & GitHub | Version control |

---

## ✅ Implemented Features

- [x] Interactive Streamlit chatbot.
- [x] Local LLM integration using Ollama.
- [x] Llama 3.2 inference without OpenAI API credits.
- [x] Basic prompt injection detection.
- [x] PII detection using Microsoft Presidio.
- [x] Automatic PII anonymization before LLM processing.
- [x] Basic role-based access checks.
- [x] Security event logging.
- [x] Basic security test cases.

---

## 🚀 Proposed Enhancements

- [ ] Multi-signal security risk scoring.
- [ ] Context-aware prompt injection detection.
- [ ] Adaptive security response mechanisms.
- [ ] Explainable AI security decisions.
- [ ] Indirect prompt injection detection in uploaded documents.
- [ ] Privacy-aware conversation management.
- [ ] Interactive security monitoring dashboard.
- [ ] Security evaluation using malicious and benign prompt datasets.
- [ ] Performance evaluation using detection accuracy, false-positive rate and response latency.
- [ ] AWS cloud deployment.

---

## 📂 Project Structure

```text
SecureGenAI/
│
├── app.py
├── security.py
├── test_security.py
├── test_ollama.py
├── test_openai.py
├── .env
├── .gitignore
│
└── logs/
    └── security.log
```

**Note:** The `.env` file, virtual environment and security logs should not be uploaded to GitHub.

---

## ⚙️ Installation and Setup

### 1. Clone the repository

```bash
git clone YOUR_GITHUB_REPOSITORY_URL
cd SecureGenAI
```

### 2. Create a virtual environment

```bash
python -m venv venv
```

Activate it on Windows:

```powershell
.\venv\Scripts\Activate.ps1
```

### 3. Install dependencies

```bash
pip install streamlit langchain langchain-ollama python-dotenv presidio-analyzer presidio-anonymizer
```

### 4. Install Ollama

Download Ollama:

https://ollama.com/download/windows

Download the model:

```bash
ollama pull llama3.2:1b
```

### 5. Configure environment variables

Create a `.env` file:

```env
APP_ROLE=analyst
```

### 6. Run the application

```bash
streamlit run app.py
```

---

## 🧪 Security Testing

The current prototype includes tests for:

| Test Case | Expected Behaviour |
|---|---|
| Normal prompt | Request allowed |
| Prompt injection | Suspicious request blocked |
| Email detection | Email anonymized |
| Authorized role | Access permitted |
| Unauthorized role | Access denied |

---

## 🔬 Research and Evaluation

The proposed adaptive framework will be evaluated against the current rule-based implementation.

Evaluation metrics will include:

- Detection accuracy.
- Precision and recall.
- False-positive rate.
- Response latency.
- Security decision consistency.

The objective is to investigate whether context-aware risk assessment can improve the reliability of security controls in local Generative AI applications.

---

## 🔒 Security Disclaimer

SecureGenAI is an educational and research prototype. Its current detection mechanisms are limited and do not guarantee protection against all prompt injection attacks, privacy leaks, or other LLM security threats.

It should not be used to process confidential production data without additional security testing and controls.

---

## 👩‍💻 Project Status

**Current Stage:** Working prototype with local LLM integration and basic security controls.

**Next Stage:** Development of the Context-Aware Adaptive Security Engine.

**Project Domain:** Artificial Intelligence | Generative AI Security | Cybersecurity | Privacy Engineering

---

*Built as an exploration of practical security challenges in Generative AI applications.*
