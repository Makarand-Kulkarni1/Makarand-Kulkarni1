<h1 align="center">Hi, I'm Makarand Kulkarni 👋</h1>
<h3 align="center">AI / ML Engineer · I build, break, debug and ship ML and GenAI systems</h3>

<p align="center">
  Pune, India · Open to entry-level <b>AI / GenAI / ML Engineer</b>, <b>Data Scientist</b> and <b>Python</b> roles (on-site Pune or remote)
</p>

<p align="center">
  <a href="https://www.linkedin.com/in/makarand-kulkarni-data"><img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white"></a>
  <a href="mailto:makarandk241@gmail.com"><img src="https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white"></a>
</p>

---

## 👨‍💻 About

I'm a B.Tech Computer Science graduate (2026) and Data Science Intern at Greateway Software. I build ML and GenAI systems end to end: data, training, retrieval, evaluation and deployment.

What I care about most is **why a model fails**. Across my projects I have caught data leakage, memorization, a retrieval chunking bug and a production outage, and fixed each one with a measured before/after result.

- 🔭 Working on: agentic LLM systems and self-monitoring ML pipelines
- 🌱 Learning: MLOps, cloud deployment, time-series forecasting, and data structures and algorithms
- 💬 Ask me about: RAG chunking, data leakage, evaluating LLMs fairly, or a "works locally, fails in the cloud" bug

---

## ⭐ Projects at a glance

| Project | What it does | Key result | Links |
|---|---|---|---|
| 🧪 **Autonomous Data Scientist Agent** | Multi-agent system: CSV + plain-English goal → trained, reviewed, deployable model | 0.9957 ROC-AUC on Breast Cancer; 0.8416 on 7,043-row Telco churn | [Code](https://github.com/Makarand-Kulkarni1/Autonomous-Data-Scientist-Agent) |
| 🧠 **Tiny Transformer Lab** | Text-to-SQL transformer trained from scratch, compared with LoRA and a 120B API model | 98.0% execution accuracy on 1,172 held-out questions | [Code](https://github.com/Makarand-Kulkarni1/Tiny_Transformer_Lab) |
| 🤖 **RAG Agent Assistant** | RAG built without a framework, with function-calling tools | Retrieval accuracy 60% → 80% after fixing a chunking bug | [Code](https://github.com/Makarand-Kulkarni1/RAG-AGENT-ASSISTANT) · [Demo](https://rag-agent-assistant-pyhyzuajlt4dinzxpmaasx.streamlit.app/) |
| 📈 **Crypto Market Regime Monitor** | Live BTC/USD regime forecast, re-run every 15 minutes | 63% accuracy vs 44% baseline after removing leakage | [Code](https://github.com/Makarand-Kulkarni1/crypto-regime-monitor-project) · [Demo](https://crypto-regime-monitor-project.streamlit.app/) |
| 🔮 **Customer Churn Prediction API** | XGBoost churn model served as a REST API | 0.837 ROC-AUC; recall 53% → 69% via threshold tuning | [Code](https://github.com/Makarand-Kulkarni1/churn-prediction-api) · [API docs](https://churn-prediction-api-7jvh.onrender.com/docs) |

---

## 🛠️ Featured work

### 🧪 [Autonomous Data Scientist Agent](https://github.com/Makarand-Kulkarni1/Autonomous-Data-Scientist-Agent)
A planner, coder, reviewer and orchestrator work together to explore a dataset, engineer features, train and compare models, and export a deployable model with a Markdown/PDF report.

- **Safe execution:** agent-written code runs in a per-run Docker sandbox with no network, CPU/memory/time limits and a read-only filesystem
- **Reviewer agent:** a regex leakage scanner plus an LLM judge. It caught a real leak (feature selection before cross-validation) that no pattern check could see
- **Reliability:** self-repair on crashes, checkpointed resumable runs, and a validated metrics contract instead of parsing printed output
- **Benchmarks:** 0.9957 (Breast Cancer), 1.0 (Wine) and 0.8416 (Telco churn) ROC-AUC. The churn score beats my own hand-built 0.837 model
- **Stack:** FastAPI, Streamlit, MLflow, pytest and GitHub Actions CI

`Python` `Docker` `FastAPI` `MLflow` `scikit-learn` `XGBoost` `Pydantic` `pytest`

### 🧠 [Tiny Transformer Lab](https://github.com/Makarand-Kulkarni1/Tiny_Transformer_Lab)
Text-to-SQL, scored by running the generated queries. I trained a decoder-only transformer from scratch (852k parameters), fine-tuned **Qwen2.5-0.5B with LoRA**, and compared both against a prompted 120B API model.

- **From scratch:** 98.0% execution accuracy on 1,172 held-out questions
- **Debugging:** near-zero loss but 39.5% validation accuracy meant the model was memorizing spellings. Word-swap augmentation lifted validation accuracy to 99.1%
- **Fair comparison:** confidence intervals and McNemar tests on identical questions. On rephrased questions: 38.0% (from scratch), 85.2% (LoRA), 93.5% (120B API)
- **Deployment:** 4-bit quantization (5.3x smaller, no measurable accuracy loss) and a CPU-only Streamlit demo

`Python` `PyTorch` `Hugging Face` `PEFT / LoRA` `SQLite` `Streamlit`

### 🤖 [RAG Agent Assistant](https://github.com/Makarand-Kulkarni1/RAG-AGENT-ASSISTANT) · [Live demo](https://rag-agent-assistant-pyhyzuajlt4dinzxpmaasx.streamlit.app/)
A Retrieval-Augmented Generation system built from first principles, with no high-level RAG framework.

- Section-aware chunking, local Sentence-Transformers embeddings and FAISS search
- Function-calling agent that decides when to use a tool instead of retrieved text
- Hand-built Q&A test set; fixing a chunking bug that split facts across chunks raised retrieval accuracy **60% → 80%**
- FastAPI backend, Streamlit dashboard, Docker container

`Python` `PyTorch` `FAISS` `Sentence-Transformers` `Groq API` `FastAPI` `Docker`

### 📈 [Crypto Market Regime Monitor](https://github.com/Makarand-Kulkarni1/crypto-regime-monitor-project) · [Live dashboard](https://crypto-regime-monitor-project.streamlit.app/)
A cloud-automated Random Forest pipeline that forecasts the BTC/USD market regime 60 minutes ahead, with a dashboard that checks its own past predictions.

- Removed a leakage bug that inflated accuracy to ~99%; the honest result is **63% vs a 44% baseline**
- GitHub Actions runs it every 15 minutes with no manual steps
- Fixed a production outage (Binance blocks US cloud IPs) by switching data source without changing downstream code

`Python` `scikit-learn` `GitHub Actions` `Streamlit` `Plotly` `SQLite`

### 🔮 [Customer Churn Prediction API](https://github.com/Makarand-Kulkarni1/churn-prediction-api) · [API docs](https://churn-prediction-api-7jvh.onrender.com/docs)
XGBoost churn model on the IBM Telco dataset, deployed with FastAPI on Render.

- Found disguised missing values (blank strings in `TotalCharges`) that a plain null check misses
- Moved the decision threshold from 0.5 to 0.35, because missing a churner costs more than a wasted offer: recall **53% → 69%**

`Python` `XGBoost` `FastAPI` `Pydantic` `Render`

### 📊 Data analysis
- [Data Analyst Job Market Analysis](https://github.com/Makarand-Kulkarni1/Data-Analyst-Job-Market-Analysis): about 15,000 postings; role demand, skills, salary by seniority and skill co-occurrence
- [Sales Revenue Decline Analysis](https://github.com/Makarand-Kulkarni1/Sales-Revenue-Decline-Analysis): root-cause analysis on a synthetic dataset, tracing a quarterly drop to rising Electronics returns

---

## 🧰 Tech stack

| Area | Tools |
|---|---|
| **Languages & data** | Python, SQL, Pandas, NumPy |
| **ML** | scikit-learn, XGBoost, Random Forest, feature engineering, threshold tuning, statistical testing |
| **GenAI / LLM** | PyTorch, Hugging Face, LoRA / PEFT, RAG, FAISS, embeddings, function calling, LLM evaluation, quantization |
| **Deployment** | FastAPI, Pydantic, Docker, Render, GitHub Actions, Streamlit, MLflow |
| **Visualization** | Matplotlib, Seaborn, Plotly, Power BI |

<p>
  <img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white">
  <img src="https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white">
  <img src="https://img.shields.io/badge/Hugging_Face-FFD21E?style=flat-square&logo=huggingface&logoColor=black">
  <img src="https://img.shields.io/badge/scikit--learn-F7931E?style=flat-square&logo=scikitlearn&logoColor=white">
  <img src="https://img.shields.io/badge/XGBoost-006400?style=flat-square">
  <img src="https://img.shields.io/badge/Pandas-150458?style=flat-square&logo=pandas&logoColor=white">
  <img src="https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white">
  <img src="https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white">
  <img src="https://img.shields.io/badge/Streamlit-FF4B4B?style=flat-square&logo=streamlit&logoColor=white">
  <img src="https://img.shields.io/badge/MLflow-0194E2?style=flat-square&logo=mlflow&logoColor=white">
  <img src="https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white">
  <img src="https://img.shields.io/badge/SQL-4479A1?style=flat-square&logo=mysql&logoColor=white">
  <img src="https://img.shields.io/badge/Power_BI-F2C811?style=flat-square&logo=powerbi&logoColor=black">
  <img src="https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white">
</p>

---

<p align="center">📫 <b>makarandk241@gmail.com</b> · <a href="https://www.linkedin.com/in/makarand-kulkarni-data">LinkedIn</a></p>
