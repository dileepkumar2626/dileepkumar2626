<h1 align="center">Hi, I'm Dileep Kumar 👋</h1>

<h3 align="center">AI / ML Engineer · LLM Agents · Generative AI · Computer Vision</h3>

<p align="center">
  CS student at the University of Debrecen (Faculty of Informatics) · Based in Budapest, Hungary 🇭🇺
</p>

<p align="center">
  <a href="https://www.linkedin.com/in/dileep-kumarbh/"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"></a>
  <a href="mailto:dileepkumarbh5175@gmail.com"><img src="https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white" alt="Email"></a>
  <a href="https://adain-neural-style-transfer-nc755sseypejksgcwxs7ec.streamlit.app/"><img src="https://img.shields.io/badge/Live%20Demo-StyleForge%20AI-FF4B4B?style=for-the-badge&logo=streamlit&logoColor=white" alt="StyleForge AI live demo"></a>
</p>

---

## 👨‍💻 About Me

I like taking a model all the way from raw data to something people can use: cleaning the data, training the model,
putting it behind an API, building the interface, and packaging it with Docker. Lately I've been building **LLM agents**,
and I care about measuring them, not just demoing them.

- 🤖 **AI Agents & Automation Intern at AgenticX AI Labs**: built a tool-using research agent, a RAG question-answering service with page-level citations, and an MCP server, each with its own evaluation suite
- 🖌️ Built **StyleForge AI**, an AdaIN neural style transfer app with a [live demo](https://adain-neural-style-transfer-nc755sseypejksgcwxs7ec.streamlit.app/), 65 preset styles and face preservation
- 🎨 Built a **CycleGAN from scratch in PyTorch** and turned it into a full-stack face-to-anime app
- 📊 Reached **93.6% recall** predicting customer churn on **36,000+ records**
- 🎮 Trained a **Deep Q-Network** agent to play Flappy Bird from reward signals alone
- 🏅 **9 NVIDIA Deep Learning Institute certificates**, plus NVIDIA, Microsoft, IBM, Cisco and Certiport certifications

---

## 💼 Experience

### 🤖 AI Agents & Automation Intern · AgenticX AI Labs (virtual) · Oct – Nov 2026
A 4-week remote programme with three projects, each reviewed independently against published criteria.

#### 🔎 [Tool-Using Research Agent](https://github.com/dileepkumar2626/project2)
> Searches the web, reads pages, and writes a cited summary, and stops when it has enough.

- A **decide → act → observe** loop on Claude tool use with `search` (DuckDuckGo), `fetch` (httpx + trafilatura) and an explicit `finish` tool
- **Cost control outside the model**: a hard iteration cap and a total token budget per run
- A **scratchpad** keeps context small: pages are truncated, and short summaries of findings are fed back every turn
- Failed fetches come back as **observations, not exceptions**, so the agent adapts. Repeated queries and URLs are blocked, and every tool call is validated
- A **10-question benchmark** tracks completion, sources cited, expected domains, iterations and tokens

`Python` `Claude API` `Tool Use` `httpx` `trafilatura`

#### 📄 [PDF Question-Answering Agent (RAG)](https://github.com/dileepkumar2626/project1)
> Ask questions about a folder of PDFs and get answers with the page they came from.

- **Structure-aware chunking**: chunks keep their page number and section heading, and the title and heading are prepended before embedding
- **Sentence Transformers** embeddings in **ChromaDB**, with Claude generating answers and **page-level citations**
- **FastAPI** endpoints to ingest a folder, upload a file, ask, and list or delete documents, plus a health check
- **Hash-based caching** skips unchanged files, and scanned PDFs are detected rather than answered from empty context
- A **20-question evaluation** scores **retrieval** and **generation** separately, so you know which stage to fix

`Python` `RAG` `ChromaDB` `Sentence Transformers` `FastAPI` `Claude API`

#### 🔌 [MCP Documentation Server](https://github.com/dileepkumar2626/project3)
> Lets any MCP client (Claude Desktop, Claude Code…) answer questions about a docs folder.

- A read-only **Model Context Protocol** server over stdio with three narrow tools: `search_docs`, `read_doc`, `list_sections`
- A custom **keyword search engine**: TF-IDF with length normalisation, an IDF threshold, stop words, word-form and British/American spelling expansion, and a phrase-match bonus
- A **15-question eval suite**, used to iterate on tool descriptions

`Python` `MCP` `TF-IDF` `Claude Desktop` `Claude Code`

---

## 🚀 Projects

### 🖌️ [StyleForge AI: AdaIN Neural Style Transfer](https://github.com/dileepkumar2626/AdaIN-Neural-Style-Transfer) · Generative AI · [Live Demo](https://adain-neural-style-transfer-nc755sseypejksgcwxs7ec.streamlit.app/)
> Repaint any photo in the style of any other image, in real time, with no per-style training.

- **Arbitrary style transfer with Adaptive Instance Normalization** (Huang & Belongie, ICCV 2017): a frozen VGG-19 encoder, an AdaIN layer that matches channel-wise style statistics, and a decoder trained in PyTorch
- **Decoder trained for 192 epochs** with content + multi-layer style losses (Adam, learning-rate decay), including resuming from saved decoder/optimizer checkpoints
- **Adjustable style strength** (`alpha` 0–1) and a library of **65 preset styles** across 12 categories, or upload your own style image
- **Face preservation**: MediaPipe Face Mesh (with an OpenCV Haar-cascade fallback) builds a face mask, and a feathered blend keeps facial detail recognisable
- **Flask web app** with accounts and history: hashed passwords, signed password-reset tokens, CSRF protection, rate limiting, per-user uploads, SQLite/PostgreSQL via SQLAlchemy, Gunicorn
- **Streamlit demo** deployed online: no login, 256/384/512 px processing, before/after slider, PNG download

`PyTorch` `AdaIN` `VGG-19` `MediaPipe` `OpenCV` `Flask` `Streamlit` `PostgreSQL`

---

### 🎨 [Face → Anime AI](https://github.com/dileepkumar2626/Face-Anime-AI) · Full-Stack Generative AI
> Upload a photo of a face and get back an anime-style version, using unpaired image-to-image translation.

- **CycleGAN written from scratch**: two 9-block ResNet generators, two 70×70 PatchGAN discriminators, LSGAN + cycle-consistency + identity losses, a 50-image replay buffer, and linear learning-rate decay
- **Data pipeline**: EDA on 500k+ raw images, corruption checks, MD5 deduplication, and 80/20 splits; trained on **~41.5k anime and ~50k real faces** for 26 epochs
- **Inference**: OpenCV face detection crops the face automatically, so any normal photo works
- **FastAPI** backend serving two models (the custom CycleGAN and a pretrained **AnimeGANv2** for comparison), with lazy loading, in-memory caching, and checkpoints pulled from **Hugging Face**
- **React + Vite** frontend to upload, pick a model, transform and download
- **Docker Compose** setup: PyTorch/CUDA backend + Nginx-served frontend

`PyTorch` `CycleGAN` `OpenCV` `FastAPI` `React` `Docker` `CUDA` `Hugging Face`

---

### 📊 [Customer Churn Prediction](https://github.com/dileepkumar2626/Customer-Churn-Prediction) · Machine Learning
> Predicts which customers are likely to leave, so a business can step in before they do.

- **36,000+ customer records**: replaced invalid values (`?`, `Error`, `-999`), imputed missing data (mean or mode, depending on outliers), engineered new features (active days, combined complaint status, time spent per login day), one-hot encoding, and scaling
- Compared **Logistic Regression, Random Forest, Gradient Boosting, XGBoost and CatBoost**
- **Gradient Boosting performed best: 93.6% recall, 87.2% accuracy, 0.89 F1** on 7,399 test customers. Recall was the priority, since missing a churner costs more than a false alarm
- Hyperparameter search with RandomizedSearchCV; final model exported as a scikit-learn Pipeline
- EDA of every feature against churn risk: membership tier, feedback and complaint status were the strongest signals

`Python` `Pandas` `Scikit-learn` `Gradient Boosting` `XGBoost` `CatBoost` `Seaborn`

---

### 🎮 [Deep Q-Learning Flappy Bird](https://github.com/dileepkumar2626/reinforcement-learning-flappy-bird) · Reinforcement Learning
> A DQN agent that learns to play Flappy Bird by trial and error.

- **Deep Q-Network** (2×256 MLP) with experience replay (100k transitions), a target network synced every 1,000 steps, and epsilon-greedy exploration
- Trained for **5,000 episodes** in Gymnasium (`flappy-bird-gymnasium`); best episode reward improved from **−7.5 to 6.0**
- Train and watch modes, best-model checkpointing, reward logging and a reward-curve plot
- All hyperparameters in a YAML config, plus a version of the game you can play yourself

`PyTorch` `DQN` `Gymnasium` `Reinforcement Learning`

---

### 👥 [Customer Segmentation Pipeline](https://github.com/dileepkumar2626/customer-segmentation-pipeline) · Unsupervised Learning
> Groups customers by their characteristics without any labels.

- **10,695 customers**: missing-value imputation, one-hot encoding and standard scaling
- **PCA** down to 2 components for clustering and visualization
- Elbow method (KneeLocator) to choose **k = 4**; **K-Means** compared with **DBSCAN** and scored with the Silhouette Score
- Split into separate scripts for preprocessing, feature engineering, clustering and evaluation

`Python` `Pandas` `Scikit-learn` `PCA` `K-Means` `DBSCAN`

---

### 🕹️ [Time Loop Escape](https://github.com/nd2003/sdm2026-1) · Team Hackathon · Frontend
> A real-time, two-player co-op escape-room game in the browser, built by a student team.

- Frontend team member on a multi-team hackathon platform (**Vite + TypeScript** frontends, **Colyseus** multiplayer server on Node.js, hosted on Railway)
- Implemented local-network address detection for the room invite link, so two devices on the same Wi-Fi can join one game, with unit tests
- Merged team pull requests and kept the team branch in sync with `main` through a CI-gated branch workflow

`TypeScript` `Vite` `Colyseus` `Node.js` `Git`

---

## 🛠️ Tech Stack

**Languages**<br>
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-336791?style=for-the-badge&logo=postgresql&logoColor=white)

**LLMs & AI Agents**<br>
![Claude API](https://img.shields.io/badge/Claude%20API-191919?style=for-the-badge&logo=anthropic&logoColor=white)
![MCP](https://img.shields.io/badge/Model%20Context%20Protocol-000000?style=for-the-badge)
![RAG](https://img.shields.io/badge/RAG-4B32C3?style=for-the-badge)
![ChromaDB](https://img.shields.io/badge/ChromaDB-FF6F00?style=for-the-badge)
![Sentence Transformers](https://img.shields.io/badge/Sentence%20Transformers-FFD21E?style=for-the-badge&logo=huggingface&logoColor=black)

**Deep Learning, Generative AI & Computer Vision**<br>
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white)
![OpenCV](https://img.shields.io/badge/OpenCV-5C3EE8?style=for-the-badge&logo=opencv&logoColor=white)
![Hugging Face](https://img.shields.io/badge/Hugging%20Face-FFD21E?style=for-the-badge&logo=huggingface&logoColor=black)
![CUDA](https://img.shields.io/badge/NVIDIA%20CUDA-76B900?style=for-the-badge&logo=nvidia&logoColor=white)
![Gymnasium](https://img.shields.io/badge/Gymnasium-0081A5?style=for-the-badge)
![MediaPipe](https://img.shields.io/badge/MediaPipe-0097A7?style=for-the-badge&logo=mediapipe&logoColor=white)

**Machine Learning & Data**<br>
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white)
![XGBoost](https://img.shields.io/badge/XGBoost-EC6B00?style=for-the-badge)
![CatBoost](https://img.shields.io/badge/CatBoost-FFCC00?style=for-the-badge&logoColor=black)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-11557C?style=for-the-badge)
![Jupyter](https://img.shields.io/badge/Jupyter-F37626?style=for-the-badge&logo=jupyter&logoColor=white)

**Web, Databases & Deployment**<br>
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white)
![Flask](https://img.shields.io/badge/Flask-000000?style=for-the-badge&logo=flask&logoColor=white)
![Streamlit](https://img.shields.io/badge/Streamlit-FF4B4B?style=for-the-badge&logo=streamlit&logoColor=white)
![React](https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)
![Vite](https://img.shields.io/badge/Vite-646CFF?style=for-the-badge&logo=vite&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![Nginx](https://img.shields.io/badge/Nginx-009639?style=for-the-badge&logo=nginx&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white)
![SQLite](https://img.shields.io/badge/SQLite-003B57?style=for-the-badge&logo=sqlite&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black)
![Git](https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white)

---

## 🏅 Certifications

- **NVIDIA Deep Learning Institute (9):** Fundamentals of Deep Learning · Generative AI with Diffusion Models · Building AI Agents with Multimodal Models · Building LLM Applications With Prompt Engineering · Computer Vision for Industrial Inspection · NVIDIA Isaac for Accelerated Robotics · Fundamentals of Accelerated Data Science · AI for Anomaly Detection · AI for Predictive Maintenance
- **NVIDIA (Coursera):** AI Infrastructure and Operations Fundamentals · The Fundamentals of RDMA Programming · Introduction to Networking
- **Microsoft:** Azure Data Fundamentals (DP-900) · Security, Compliance, and Identity Fundamentals (SC-900)
- **Certiport IT Specialist:** Python · Software Development · JavaScript · HTML & CSS
- **IBM:** Generative AI Fundamentals Specialization
- **Cisco:** Linux Essentials · **Cognitive Class:** SQL and Relational Databases 101

---

## 🎓 Education & Activities

- **BSc Computer Science**, University of Debrecen, Faculty of Informatics (2024 – present) · CGPA 4.0/5.0
- Attended the **4th UD International Scientific Conference** (May 2025)

---

## 🎯 Open To

**AI/ML Engineer · LLM & AI Agents · Generative AI · Computer Vision · MLOps · AI Software Engineer** roles: internships, working-student positions and junior roles, plus **AI research** opportunities.

---

<p align="center">
  <b>Data → Model → API → App → Agent</b><br>
  📫 Let's connect: <a href="https://www.linkedin.com/in/dileep-kumarbh/">LinkedIn</a> · <a href="mailto:dileepkumarbh5175@gmail.com">Email</a>
</p>
