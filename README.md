# Hi there! 👋 I'm Anushree Udhayakumar

**AI Engineer · University of Illinois Urbana-Champaign**
Actively seeking entry-level **AI Engineer**, **Machine Learning Engineer**, and **Data Science** roles.

I build production-ready AI systems — RAG pipelines, privacy-preserving LLM middleware, multimodal fine-tuning, and forecasting engines. My work emphasizes **evaluable, reliable AI**: systems with measurable outputs, guardrails that know when to abstain, and software engineering principles baked in from day one — clean APIs, modular design, fail-safe architectures, and reproducible evaluation.

[🔗 LinkedIn](https://www.linkedin.com/in/anushree-udhayakumar-088797204/) · [📧 au11@illinois.edu](mailto:au11@illinois.edu) · [📧 uanushree013@gmail.com](mailto:uanushree013@gmail.com) · 📞 447-902-6430

---

## 🚀 Featured Projects

### 🧬 [ScholarBOT](https://github.com/AnushreeU13/ScholarBOT_Production)
**RAG · Hybrid Retrieval · LLMs · Responsible AI · NLP · Evaluation · Streamlit**

A production-grade clinical RAG system built around a **zero-hallucination, fail-closed architecture** for medical query answering.

- **Hybrid Retrieval Pipeline**: Combines dense semantic search (sentence-transformers) with sparse BM25 retrieval, fused via **Reciprocal Rank Fusion (RRF)** — balancing recall breadth with precision targeting.
- **Fail-Closed Guardrails**: Confidence-threshold checks enforce abstention over uncertain generation — a safety-critical SWE principle applied to a high-stakes clinical domain.
- **Dual Summarization**: Single evidence base produces both technical Clinician Summaries and accessible Patient-Friendly Summaries, with inline citations for full traceability.
- **Evaluation Suite**: End-to-end **RAGAS**-based pipeline measuring faithfulness, context recall, and answer relevancy — treating eval as a first-class component, not an afterthought.
- **Stack**: GPT-4o · LangChain · FAISS · BM25 · Sentence Transformers · RAGAS · Streamlit · Python 3.9+

---

### 🛡️ [PACT — Privacy-Aware Communication Tool](https://github.com/AnushreeU13/PACT)
**Privacy Engineering · NER · FastAPI · LLMs · Full-Stack · Deployed**

A deployed full-stack middleware layer that intercepts and sanitizes user prompts before they reach cloud LLMs — preventing sensitive data leakage without degrading response quality.

- **Modular NER Pipeline**: Five parallel redaction modules (identity, location, demographics, health, financial) built on spaCy and scispacy — pluggable, independently testable, and designed with **separation of concerns**.
- **Dual Deployment Architecture**: Runs fully on-device via Ollama (Llama 3.1:8B) for maximum privacy, or routes through Groq API for cloud inference — clean abstraction layer handles both without API-level changes.
- **RESTful API Backend**: FastAPI service with well-defined request/response contracts; deployed on **Railway** with a GitHub Pages frontend — demonstrating end-to-end full-stack ownership.
- **Semantic Integrity Verification**: AU-Probe scoring validates that sanitized prompts retain sufficient context for useful LLM responses, preventing over-redaction.
- **Stack**: FastAPI · spaCy · scispacy · Llama 3.1:8B · Ollama · Groq · Railway · GitHub Pages · Python · JavaScript · HTML/CSS

---

## 🛠️ More Projects

### 🖼️ [Multimodal "Cloze" in Comics](https://github.com/AnushreeU13/Experimenting-Multimodal-Cloze-in-Comics-with-Vision-Language-Model)
**Vision-Language Models · QLoRA · Fine-Tuning · PEFT · Stable Diffusion · Generative AI**

Fine-tuned LLaVA-OneVision on comic narrative understanding — achieving **+111% ROUGE-2 improvement** over zero-shot baselines.

- **Scalable Data Pipeline**: Generated ~300K silver-standard training examples using Gemini 2.5 Flash as an automated annotator — a reproducible, cost-efficient alternative to manual labeling.
- **Parameter-Efficient Fine-Tuning**: Applied **QLoRA (4-bit quantization)** on NVIDIA H200 GPUs, significantly reducing memory footprint while preserving model quality — a core PEFT technique for production fine-tuning.
- **Closed-Loop Generation**: Integrated Stable Diffusion v1.5 for panel image synthesis from predicted narrative descriptions, completing a full multimodal prediction-to-generation pipeline.

---

### 🏁 [Formula One Logistics — Red Bull Racing](https://github.com/AnushreeU13/Formula-One-Logistics-for-Red-Bull-Racing)
**Monte Carlo Simulation · PERT Distributions · Risk Modeling · Python**

Stochastic simulation engine for inter-race F1 cargo logistics — **100% on-time delivery across 500 simulation runs** (mean: 15.63 hrs) under baseline conditions.

- **Probabilistic Risk Modeling**: Four-hypothesis failure framework (crash, breakdown, weather/customs, baseline) using PERT distributions — quantifying risk exposure per scenario and isolating crash events as the dominant delay driver.
- **Decision Logic**: Automated road-vs-air freight selection based on distance, disruption type, and sustainability constraints — encoding domain-specific business logic as a deterministic rule engine.
- **Config-Driven Design**: YAML-based parameter configuration decouples simulation inputs from logic — enabling scenario sweep testing and reproducibility without code changes (SWE best practice).

---

### 🏎️ [Mercedes F1 — Infringement Profiling](https://github.com/AnushreeU13/Mercedes-Infringement-Profiling)
**NLP · Text Summarization · LLMs · Automated Evaluation · Transformers · Benchmarking**

Automated NLP summarization pipeline over 82 FIA infringement documents, benchmarking extractive vs. abstractive models against LLM-generated reference summaries.

- **LLM-as-Evaluator**: Used GPT-4o and Groq-Llama to generate silver-standard ground truths — a scalable annotation strategy replacing costly human labeling.
- **Multi-Model Benchmarking**: Compared TextRank, LexRank, DistilBART, and Pegasus on ROUGE + FactCC metrics; **DistilBART achieved best ROUGE-1 (0.330) with 99.83% factual consistency** and 89.47% entity retention.
- **Reproducible Eval Pipeline**: Modular notebook architecture separates data processing, inference, and evaluation — each stage independently rerunnable and auditable.

---

### 💳 [Credit Risk Analysis — Synchrony](https://github.com/AnushreeU13/Credit-Risk-Analysis-for-Synchrony)
**Random Forest · Classification · Feature Engineering · Predictive Modeling · Python**

End-to-end ML pipeline for Q4 customer spending forecasting and credit risk segmentation, with downstream personalized recommendations.

- **3-Tier Risk Classification**: Segmented customers into Low Risk / Watchlist / High Risk using credit bureau anomaly detection and engineered behavioral features.
- **Modular Three-Stage Pipeline**: Forecasting → risk categorization → recommendation generation, with clean separation of concerns and reproducible CSV outputs at each stage.
- **Business-Linked Output**: Translated risk tier predictions directly into personalized credit line increase recommendations — closing the loop between ML inference and actionable business decisions.

---

### 📊 [Synchrony Intraday Call Forecasting](https://github.com/AnushreeU13/Synchrony_Intraday_Call_Forecasting)
**LightGBM · Time-Series Forecasting · Quantile Regression · Feature Engineering · Python**

High-precision forecasting system for 4 call centers at 30-minute intervals — **1.48% abandon rate error** and **13.96% CCT error** on August 2025 holdout.

- **19-Feature Engineering**: Temporal, lag, staffing ratio, and daily aggregate features capturing intraday seasonality and cross-metric dependencies (slot-level correlations >0.999 across months).
- **Asymmetric Loss Optimization**: Quantile regression (α = 0.55) biases volume forecasts upward; a 1.05 calibration multiplier improved composite score **35% over baseline** — directly minimizing under-staffing risk.
- **Outlier-Robust Post-Processing**: Replaced raw predictions with 25–40% trimmed means capped at domain-validated bounds, decoupling final outputs from model extrapolation errors on sparse data.

---

## 💻 Skills & Technologies

**Languages**

![Python](https://img.shields.io/badge/Python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)

**Generative AI & LLMs**

![OpenAI](https://img.shields.io/badge/OpenAI-412991?style=for-the-badge&logo=openai&logoColor=white)
![HuggingFace](https://img.shields.io/badge/%F0%9F%A4%97%20Hugging%20Face-FFD21E?style=for-the-badge&logoColor=black)
![LangChain](https://img.shields.io/badge/LangChain-1C3C3C?style=for-the-badge&logo=langchain&logoColor=white)
![LlamaIndex](https://img.shields.io/badge/LlamaIndex-000000?style=for-the-badge&logo=llamaindex&logoColor=white)
![Groq](https://img.shields.io/badge/Groq-F55036?style=for-the-badge&logoColor=white)
![Ollama](https://img.shields.io/badge/Ollama-000000?style=for-the-badge&logoColor=white)
![Prompt Engineering](https://img.shields.io/badge/Prompt_Engineering-412991?style=for-the-badge&logoColor=white)
![Function Calling](https://img.shields.io/badge/Function_Calling-6935D3?style=for-the-badge&logoColor=white)
![Structured Outputs](https://img.shields.io/badge/Structured_Outputs-5A189A?style=for-the-badge&logoColor=white)
![Guardrails](https://img.shields.io/badge/Guardrails-3A0CA3?style=for-the-badge&logoColor=white)
![Responsible AI](https://img.shields.io/badge/Responsible_AI-4361EE?style=for-the-badge&logoColor=white)

**RAG & Vector Search**

![FAISS](https://img.shields.io/badge/FAISS-009688?style=for-the-badge&logoColor=white)
![BM25](https://img.shields.io/badge/BM25-00897B?style=for-the-badge&logoColor=white)
![Hybrid Retrieval](https://img.shields.io/badge/Hybrid_Retrieval-00796B?style=for-the-badge&logoColor=white)
![Reciprocal Rank Fusion](https://img.shields.io/badge/Reciprocal_Rank_Fusion-004D40?style=for-the-badge&logoColor=white)
![Semantic Search](https://img.shields.io/badge/Semantic_Search-26A69A?style=for-the-badge&logoColor=white)
![Sentence Transformers](https://img.shields.io/badge/Sentence_Transformers-00695C?style=for-the-badge&logoColor=white)
![Embedding Models](https://img.shields.io/badge/Embedding_Models-0097A7?style=for-the-badge&logoColor=white)
![Re-Ranking](https://img.shields.io/badge/Re--Ranking-00838F?style=for-the-badge&logoColor=white)

**Model Fine-Tuning & Training**

![PyTorch](https://img.shields.io/badge/PyTorch-%23EE4C2C.svg?style=for-the-badge&logo=PyTorch&logoColor=white)
![QLoRA](https://img.shields.io/badge/QLoRA-FF6F00?style=for-the-badge&logoColor=white)
![LoRA](https://img.shields.io/badge/LoRA-FF8F00?style=for-the-badge&logoColor=white)
![PEFT](https://img.shields.io/badge/PEFT-FFA000?style=for-the-badge&logoColor=white)
![4-bit Quantization](https://img.shields.io/badge/4--bit_Quantization-FF6D00?style=for-the-badge&logoColor=white)
![Stable Diffusion](https://img.shields.io/badge/Stable_Diffusion-E65100?style=for-the-badge&logoColor=white)
![Silver-Standard Data Gen](https://img.shields.io/badge/Silver--Standard_Data_Gen-BF360C?style=for-the-badge&logoColor=white)

**NLP**

![spaCy](https://img.shields.io/badge/spaCy-09A3D5?style=for-the-badge&logoColor=white)
![scispaCy](https://img.shields.io/badge/scispaCy-0077B6?style=for-the-badge&logoColor=white)
![NLTK](https://img.shields.io/badge/NLTK-7B1FA2?style=for-the-badge&logoColor=white)
![Named Entity Recognition](https://img.shields.io/badge/Named_Entity_Recognition-6A1B9A?style=for-the-badge&logoColor=white)
![Text Summarization](https://img.shields.io/badge/Text_Summarization-7B1FA2?style=for-the-badge&logoColor=white)
![DistilBART](https://img.shields.io/badge/DistilBART-8E24AA?style=for-the-badge&logoColor=white)
![Pegasus](https://img.shields.io/badge/Pegasus-9C27B0?style=for-the-badge&logoColor=white)
![LLaVA](https://img.shields.io/badge/LLaVA--OneVision-AB47BC?style=for-the-badge&logoColor=white)
![TextRank](https://img.shields.io/badge/TextRank-6A1B9A?style=for-the-badge&logoColor=white)
![LexRank](https://img.shields.io/badge/LexRank-4A148C?style=for-the-badge&logoColor=white)

**Machine Learning & Data Science**

![scikit-learn](https://img.shields.io/badge/scikit--learn-%23F7931E.svg?style=for-the-badge&logo=scikit-learn&logoColor=white)
![Pandas](https://img.shields.io/badge/pandas-%23150458.svg?style=for-the-badge&logo=pandas&logoColor=white)
![NumPy](https://img.shields.io/badge/numpy-%23013243.svg?style=for-the-badge&logo=numpy&logoColor=white)
![LightGBM](https://img.shields.io/badge/LightGBM-2980B9?style=for-the-badge&logoColor=white)
![Random Forest](https://img.shields.io/badge/Random_Forest-1565C0?style=for-the-badge&logoColor=white)
![Feature Engineering](https://img.shields.io/badge/Feature_Engineering-1976D2?style=for-the-badge&logoColor=white)
![Time-Series Forecasting](https://img.shields.io/badge/Time--Series_Forecasting-0288D1?style=for-the-badge&logoColor=white)
![Quantile Regression](https://img.shields.io/badge/Quantile_Regression-0277BD?style=for-the-badge&logoColor=white)
![Monte Carlo Simulation](https://img.shields.io/badge/Monte_Carlo_Simulation-01579B?style=for-the-badge&logoColor=white)
![Statistical Modeling](https://img.shields.io/badge/Statistical_Modeling-004D40?style=for-the-badge&logoColor=white)
![Anomaly Detection](https://img.shields.io/badge/Anomaly_Detection-006064?style=for-the-badge&logoColor=white)

**Evaluation & Observability**

![RAGAS](https://img.shields.io/badge/RAGAS-C62828?style=for-the-badge&logoColor=white)
![ROUGE](https://img.shields.io/badge/ROUGE-D32F2F?style=for-the-badge&logoColor=white)
![FactCC](https://img.shields.io/badge/FactCC-E53935?style=for-the-badge&logoColor=white)
![Semantic Similarity](https://img.shields.io/badge/Semantic_Similarity-EF5350?style=for-the-badge&logoColor=white)
![Hallucination Detection](https://img.shields.io/badge/Hallucination_Detection-B71C1C?style=for-the-badge&logoColor=white)
![Confidence Thresholds](https://img.shields.io/badge/Confidence_Thresholds-C62828?style=for-the-badge&logoColor=white)
![Model Benchmarking](https://img.shields.io/badge/Model_Benchmarking-D32F2F?style=for-the-badge&logoColor=white)
![LLM-as-Evaluator](https://img.shields.io/badge/LLM--as--Evaluator-E53935?style=for-the-badge&logoColor=white)

**Backend & APIs**

![FastAPI](https://img.shields.io/badge/FastAPI-005571?style=for-the-badge&logo=fastapi)
![Streamlit](https://img.shields.io/badge/Streamlit-FF4B4B?style=for-the-badge&logo=streamlit&logoColor=white)
![REST API Design](https://img.shields.io/badge/REST_API_Design-005571?style=for-the-badge&logoColor=white)
![API Contract Design](https://img.shields.io/badge/API_Contract_Design-00695C?style=for-the-badge&logoColor=white)
![Modular Pipelines](https://img.shields.io/badge/Modular_Pipeline_Architecture-00796B?style=for-the-badge&logoColor=white)

**Infrastructure & DevOps**

![Docker](https://img.shields.io/badge/Docker-%230db7ed.svg?style=for-the-badge&logo=docker&logoColor=white)
![Git](https://img.shields.io/badge/Git-%23F05033.svg?style=for-the-badge&logo=git&logoColor=white)
![AWS](https://img.shields.io/badge/AWS-232F3E?style=for-the-badge&logo=amazonaws&logoColor=white)
![Railway](https://img.shields.io/badge/Railway-0B0D0E?style=for-the-badge&logo=railway&logoColor=white)
![GitHub Pages](https://img.shields.io/badge/GitHub_Pages-222222?style=for-the-badge&logo=github&logoColor=white)
![Containerization](https://img.shields.io/badge/Containerization-0db7ed?style=for-the-badge&logoColor=white)
![Cloud Deployment](https://img.shields.io/badge/Cloud_Deployment-232F3E?style=for-the-badge&logoColor=white)

**Software Engineering Practices**

![Modular System Design](https://img.shields.io/badge/Modular_System_Design-37474F?style=for-the-badge&logoColor=white)
![Separation of Concerns](https://img.shields.io/badge/Separation_of_Concerns-455A64?style=for-the-badge&logoColor=white)
![Fail-Closed Architectures](https://img.shields.io/badge/Fail--Closed_Architectures-546E7A?style=for-the-badge&logoColor=white)
![Config-Driven Systems](https://img.shields.io/badge/Config--Driven_Systems-607D8B?style=for-the-badge&logoColor=white)
![Reproducible ML Pipelines](https://img.shields.io/badge/Reproducible_ML_Pipelines-37474F?style=for-the-badge&logoColor=white)
![Clean API Design](https://img.shields.io/badge/Clean_API_Design-455A64?style=for-the-badge&logoColor=white)
![Version Control](https://img.shields.io/badge/Version_Control-F05033?style=for-the-badge&logo=git&logoColor=white)
![Agile Development](https://img.shields.io/badge/Agile_Development-0052CC?style=for-the-badge&logoColor=white)

---

⭐️ Built by [AnushreeU13](https://github.com/AnushreeU13) · Open to **AI Engineer · ML Engineer · Data Scientist** roles
