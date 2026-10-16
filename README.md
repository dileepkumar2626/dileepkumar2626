<h1 align="center">Hi, I'm Dileep Kumar 👋</h1>

<h3 align="center">AI / ML Engineer · Generative AI · Computer Vision · Deep Learning</h3>

<p align="center">
  CS student at the University of Debrecen (CGPA 4.0/5.0) · Based in Budapest, Hungary 🇭🇺
</p>

<p align="center">
  <a href="https://www.linkedin.com/in/dileep-kumarbh/"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"></a>
  <a href="mailto:dileepkumarbh5175@gmail.com"><img src="https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white" alt="Email"></a>
</p>

---

## 👨‍💻 About Me

I build **end-to-end AI systems**: I train the model, wrap it in an API, build the interface, and ship it in a container.

- 🎨 Implemented **CycleGAN from scratch in PyTorch** and deployed it as a full-stack, GPU-enabled app
- 📊 Built ML pipelines on **36,000+ records**, reaching ~**93% recall** for churn prediction
- 🎮 Trained a **Deep Q-Network** agent to play Flappy Bird using experience replay and target networks
- 🏅 NVIDIA-certified in **Diffusion Models** and **Multimodal AI Agents**
- 🔭 Currently exploring: **RAG / LLM applications, MLOps (CI/CD, cloud deployment), and adversarial ML**

---

## 🚀 Featured Projects

### 🎨 [Face-to-Anime AI](https://github.com/dileepkumar2626/Face-Anime-AI): Full-Stack Generative AI App
> Turns a photo of a real face into an anime-style image using unpaired image-to-image translation.

- **CycleGAN built from scratch in PyTorch**: 9-block ResNet generators, PatchGAN discriminators, LSGAN loss, cycle-consistency and identity losses, replay buffer, learning-rate decay
- Full pipeline: custom Dataset/DataLoader, augmentation, 256×256 preprocessing, OpenCV face detection and cropping, checkpointing, CUDA-accelerated training and inference
- **FastAPI** backend with model selection, lazy checkpoint loading, model caching, health checks, and Swagger docs
- **React/Vite** frontend for upload, preview, generation, and download
- Integrates custom CycleGAN and pretrained **AnimeGANv2**; checkpoints hosted on **Hugging Face**
- **Dockerized** with Docker Compose (PyTorch/CUDA backend + React/Nginx frontend)

`PyTorch` `CycleGAN` `FastAPI` `React` `Docker` `CUDA` `OpenCV` `Hugging Face`

---

### 📊 [Customer Churn Prediction](https://github.com/dileepkumar2626/Customer-Churn-Prediction)
> End-to-end ML pipeline to identify customers at risk of leaving.

- Dataset of **36,000+ customer records**: imputation, anomaly handling, feature engineering, scaling
- Benchmarked **15+ algorithms**; tuned with GridSearchCV and RandomizedSearchCV
- **~93% recall** with LightGBM; recall-focused to support proactive retention
- EDA and feature-importance analysis to find the main churn drivers

`Python` `Scikit-learn` `LightGBM` `XGBoost` `CatBoost` `Pandas`

---

### 🎮 [Deep Q-Learning Flappy Bird Agent](https://github.com/dileepkumar2626/reinforcement-learning-flappy-bird)
> A DQN agent that learns to play Flappy Bird from reward signals alone.

- Experience replay, target-network synchronization, epsilon-greedy exploration
- Bellman-equation Q-value updates
- Training, evaluation, and checkpointing pipelines with reward logging and visualization

`PyTorch` `Deep Q-Networks` `Reinforcement Learning`

---

### 👥 [Customer Segmentation Pipeline](https://github.com/dileepkumar2626/customer-segmentation-pipeline)
> Unsupervised pipeline for discovering customer groups.

- K-Means (compared with DBSCAN), evaluated with Silhouette Score
- PCA for dimensionality reduction and cluster visualization
- Segments such as high-value, budget-conscious, and underutilized high-income customers

`Python` `Scikit-learn` `K-Means` `DBSCAN` `PCA`

---

### 🩺 [Skin Lesion Research](https://github.com/dileepkumar2626/SkinLesionResearch)
> Deep learning experiments in medical image classification.

- CNN-based classification, image preprocessing, model training and evaluation

`PyTorch` `CNN` `Computer Vision`

---

## 🛠️ Tech Stack

**Languages**<br>
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-336791?style=for-the-badge&logo=postgresql&logoColor=white)

**Deep Learning & Generative AI**<br>
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white)
![TensorFlow](https://img.shields.io/badge/TensorFlow-FF6F00?style=for-the-badge&logo=tensorflow&logoColor=white)
![OpenCV](https://img.shields.io/badge/OpenCV-5C3EE8?style=for-the-badge&logo=opencv&logoColor=white)
![Hugging Face](https://img.shields.io/badge/Hugging%20Face-FFD21E?style=for-the-badge&logo=huggingface&logoColor=black)
![CUDA](https://img.shields.io/badge/NVIDIA%20CUDA-76B900?style=for-the-badge&logo=nvidia&logoColor=white)

**Machine Learning & Data**<br>
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white)
![XGBoost](https://img.shields.io/badge/XGBoost-EC6B00?style=for-the-badge)
![LightGBM](https://img.shields.io/badge/LightGBM-9ACD32?style=for-the-badge)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white)

**Backend, Deployment & Tools**<br>
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white)
![React](https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![Nginx](https://img.shields.io/badge/Nginx-009639?style=for-the-badge&logo=nginx&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=for-the-badge&logo=redis&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black)

**LLM Tooling**<br>
![LangChain](https://img.shields.io/badge/LangChain-1C3C3C?style=for-the-badge&logo=langchain&logoColor=white)
![ChromaDB](https://img.shields.io/badge/ChromaDB-FF6446?style=for-the-badge)

---

## 🏅 Certifications

- **NVIDIA:** Generative AI with Diffusion Models · Building AI Agents with Multimodal Models · AI for Anomaly Detection · AI for Predictive Maintenance
- **IBM:** Generative AI Fundamentals
- **Microsoft:** Security, Compliance, and Identity Fundamentals (SC-900)
- **Certiport:** Software Development · JavaScript · HTML & CSS

---

## 🎯 Open To

**AI/ML Engineer · Generative AI Engineer · Computer Vision · AI Software Engineer · MLOps (junior)**
Internships, working-student positions, and junior roles.

---

## 📈 GitHub Stats

<p align="center">
  <img height="165" src="https://github-readme-stats.vercel.app/api?username=dileepkumar2626&show_icons=true&theme=tokyonight&hide_border=true" alt="GitHub stats" />
  <img height="165" src="https://github-readme-stats.vercel.app/api/top-langs/?username=dileepkumar2626&layout=compact&theme=tokyonight&hide_border=true" alt="Top languages" />
</p>

---

<p align="center">
  <b>Build → Experiment → Ship → Learn</b><br>
  📫 Let's connect: <a href="https://www.linkedin.com/in/dileep-kumarbh/">LinkedIn</a> · <a href="mailto:dileepkumarbh5175@gmail.com">Email</a>
</p>
