<h1 align="center">Hi, I'm Dileep Kumar 👋</h1>

<h3 align="center">AI / ML Engineer · Deep Learning · Generative AI · Computer Vision</h3>

<p align="center">
  CS student at the University of Debrecen · Based in Budapest, Hungary 🇭🇺
</p>

<p align="center">
  <a href="https://www.linkedin.com/in/dileep-kumarbh/"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"></a>
  <a href="mailto:dileepkumarbh5175@gmail.com"><img src="https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white" alt="Email"></a>
</p>

---

## 👨‍💻 About Me

I like taking a model all the way from raw data to something people can use: cleaning the data, training the model,
putting it behind an API, building the interface, and packaging it with Docker.

- 🖌️ Built **StyleForge AI**, an AdaIN neural style transfer app with a [live demo](https://adain-neural-style-transfer-nc755sseypejksgcwxs7ec.streamlit.app/), 65 preset styles and face preservation
- 🎨 Built a **CycleGAN from scratch in PyTorch** and turned it into a full-stack face-to-anime app
- 📊 Reached **93.6% recall** predicting customer churn on **36,000+ records**
- 🎮 Trained a **Deep Q-Network** agent to play Flappy Bird from reward signals alone
- 👥 Built a modular **unsupervised segmentation pipeline** with PCA, K-Means and DBSCAN

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

## 🛠️ Tech Stack

**Languages**<br>
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)

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
![Git](https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white)

---

## 🏅 Certifications

- **NVIDIA:** Generative AI with Diffusion Models · Building AI Agents with Multimodal Models · AI for Anomaly Detection · AI for Predictive Maintenance
- **IBM:** Generative AI Fundamentals
- **Microsoft:** Security, Compliance, and Identity Fundamentals (SC-900)
- **Certiport:** Software Development · JavaScript · HTML & CSS

---

## 🎯 Open To

**AI/ML Engineer · Generative AI · Computer Vision · AI Software Engineer** roles: internships, working-student positions and junior roles.

---

<p align="center">
  <b>Data → Model → API → App</b><br>
  📫 Let's connect: <a href="https://www.linkedin.com/in/dileep-kumarbh/">LinkedIn</a> · <a href="mailto:dileepkumarbh5175@gmail.com">Email</a>
</p>
