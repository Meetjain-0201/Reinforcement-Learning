# Autonomous Vehicle Racing Optimization  

🚗 **Train autonomous agents to master 2D race tracks using Q-Learning and DQN!**  

---

## 📌 Overview  
This project explores Reinforcement Learning (RL) in the **Gymnasium CarRacing-v3** environment by comparing two approaches:  
- **Tabular Q-Learning** (discretized state space)  
- **Deep Q-Network (DQN)** (CNN-based visual input processing)  

The goal is to develop agents that learn optimal driving policies through trial and error on tracks of varying complexity.  

---

## ✨ Features  

### 🏎️ **Environment**  
- **Gymnasium CarRacing-v3** – A 2D continuous-control racing environment adapted for RL.  

### 🤖 **Agents**  
- **Tabular Q-Learning**  
  - State discretization  
  - Epsilon-greedy exploration  
- **Deep Q-Network (DQN)**  
  - Convolutional Neural Network (CNN) for pixel inputs  
  - Experience replay buffer  
  - Target network synchronization  

### 📊 **Training & Analytics**  
- Reward & episode length tracking  
- Exploration rate (ε) decay visualization  
- Model checkpointing & evaluation  

### 📂 **Project Structure**  
```
├── DQN/                 # Deep Q-Network Implementation  
│   ├── DeepQ.py         # DQN agent  
│   ├── ImageProcessing.py  # Preprocessing for CNN  
│   ├── checkpoints/     # Saved models  
│   ├── main.py          # Training script  
│   └── plots/           # Training metrics & graphs  
├── Q_Learning/          # Tabular Q-Learning  
│   ├── main.py          # Training script  
│   ├── qlearning.py     # Q-Learning agent  
│   └── test_policy.py   # Policy evaluation  
├── Prev_Codebase/       # Legacy implementations  
├── requirements.txt     # Dependencies  
└── resources/           # Additional assets  
```

---

## 🛠️ Setup  

### 1. Clone & Enter  
```bash
git clone https://github.com/PranavViswanathan/FAI-Project.git
cd FAI-Project
```

### 2. Create Virtual Environment  
```bash
python3 -m venv venv
source venv/bin/activate  # Linux/Mac
# OR
.\venv\Scripts\activate  # Windows
```

### 3. Install Dependencies  
```bash
pip install -r requirements.txt
```

### (Optional) Rendering Support  
For video recording & rendering:  
```bash
sudo apt-get install ffmpeg xvfb  # Linux
```

---

## 🚀 Training  

### 🧠 **Q-Learning**  
```bash
python Q_Learning/main.py
```
- Adjust hyperparameters (`alpha`, `gamma`, `epsilon_decay`) in the script.  

### 🧠 **DQN**  
```bash
python DQN/main.py
```
- Uses CNN to process raw pixels.  
- Saves model checkpoints in `DQN/checkpoints/`.  

---

## 📊 Evaluation & Visualization  

### ▶️ Watch Trained Agents  
Test the learned policies:  

**Q-Learning Agent**  
```bash
python Q_Learning/test_policy.py
```  

**DQN Agent**  
```bash
python DQN/test_policy.py
```  

### 📈 View Training Metrics  
- Check `DQN/plots/` and `Q_Learning/metrics.csv` for performance graphs.  

---

## 🔧 Customization  
- Modify hyperparameters in `main.py` for both agents.  
- Adjust state discretization in Q-Learning for finer control.  
- Tweak CNN architecture in `DQN/DeepQ.py`.  

---

## 📜 License  
MIT License – Free for academic & personal use.  

---

🚀 **Happy Racing!** 🏁
