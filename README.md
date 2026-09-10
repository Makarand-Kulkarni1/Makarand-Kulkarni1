<h1 align="center">Hi, I'm Makarand Kulkarni 👋</h1>
<h3 align="center">AI/ML Engineer | Building & deploying live ML and GenAI systems.</h3>

<p align="center">
  <a href="https://www.linkedin.com/in/makarand-kulkarni-data"><img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white"></a>
  <a href="mailto:makarandk241@gmail.com"><img src="https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white"></a>
</p>

---

### 🚀 About Me

I build end-to-end machine learning and GenAI systems — from data ingestion and feature engineering through model training, retrieval, evaluation, and **production deployment**. I care as much about catching a data-leakage bug or diagnosing a production outage as I do about the model itself.

- 🔭 Currently building agentic LLM systems and live, self-monitoring ML pipelines
- 🌱 Deepening my skills in MLOps, cloud deployment, and time-series forecasting
- 💬 Ask me about RAG chunking strategies, data leakage, chronological validation, or debugging a "works locally, fails in the cloud" problem
- 📫 Reach me at **makarandk241@gmail.com**

---

### 🛠️ Featured Projects

#### 🤖 [RAG Agent Assistant](https://github.com/Makarand-Kulkarni1/RAG-AGENT-ASSISTANT) [Live Dashboard →]https://rag-agent-assistant-pyhyzuajlt4dinzxpmaasx.streamlit.app/
A Retrieval-Augmented Generation system built **from first principles** — no high-level RAG framework — combining document retrieval, agentic tool-use, evaluation, and a live dashboard.
- Engineered a RAG pipeline using **section-aware document chunking**, local embeddings (**Sentence-Transformers**), and **FAISS** vector search to generate grounded answers over custom documents
- Extended the assistant with **agentic tool-use** via function-calling (Groq LLM API), letting the model decide when to call external tools instead of relying solely on retrieved text
- Built a retrieval evaluation pipeline with a hand-built Q&A test set; diagnosed a **chunking bug** fragmenting facts across chunk boundaries, improving retrieval accuracy from **60% to 80%**
- Containerized with **Docker**, served via **FastAPI**, with a **Streamlit** dashboard for querying, query-log inspection, and on-demand evaluation runs

`Python` `PyTorch` `FAISS` `Sentence-Transformers` `Groq LLM API` `FastAPI` `Docker` `Streamlit`

#### 📊 [Crypto Market Regime Monitor](https://github.com/Makarand-Kulkarni1/crypto-regime-monitor-project) — [Live Dashboard →](https://crypto-regime-monitor-project.streamlit.app/)
A live, cloud-automated ML pipeline forecasting BTC/USD market regime 60 minutes ahead using a **Random Forest classifier**.
- Diagnosed and fixed a **data-leakage bug** that had inflated accuracy to a misleading ~99%; rebuilt to a defensible **63% accuracy vs. a 44% baseline**
- Fully automated via **GitHub Actions** (15-min cron) — fetches live data, predicts, and logs results unattended
- Diagnosed and resolved a **production outage** caused by a geo-blocked API dependency (Binance blocks US-based cloud IPs) by migrating data sources with zero downstream code changes
- Built a **Streamlit dashboard** with closed-loop accuracy monitoring — comparing past predictions against real outcomes, live

`Python` `scikit-learn` `Pandas` `SQLite` `GitHub Actions` `Streamlit` `Plotly`

#### 🔮 [Customer Churn Prediction API](https://github.com/Makarand-Kulkarni1/churn-prediction-api) — [Live API Docs →](https://churn-prediction-api-7jvh.onrender.com/docs)
An **XGBoost** classifier deployed as a REST API predicting telecom customer churn.
- **0.837 ROC-AUC** on IBM's Telco Customer Churn dataset (7,043 customers)
- Diagnosed a hidden **data-quality bug** — disguised missing values that would silently pass a basic null check
- Tuned the classification threshold (0.5 → 0.35) via precision-recall analysis, raising recall from **53% to 69%**
- Deployed with **FastAPI** + Pydantic validation and interactive Swagger docs on Render.

`Python` `XGBoost` `FastAPI` `Pydantic` `Render`

---

### 🧰 Tech Stack

<p>
  <img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white">
  <img src="https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white">
  <img src="https://img.shields.io/badge/scikit--learn-F7931E?style=flat-square&logo=scikitlearn&logoColor=white">
  <img src="https://img.shields.io/badge/XGBoost-006400?style=flat-square">
  <img src="https://img.shields.io/badge/FAISS-4B8BBE?style=flat-square">
  <img src="https://img.shields.io/badge/Pandas-150458?style=flat-square&logo=pandas&logoColor=white">
  <img src="https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white">
  <img src="https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white">
  <img src="https://img.shields.io/badge/Streamlit-FF4B4B?style=flat-square&logo=streamlit&logoColor=white">
  <img src="https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white">
  <img src="https://img.shields.io/badge/SQL-4479A1?style=flat-square&logo=mysql&logoColor=white">
  <img src="https://img.shields.io/badge/Power_BI-F2C811?style=flat-square&logo=powerbi&logoColor=black">
  <img src="https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white">
</p>

---
