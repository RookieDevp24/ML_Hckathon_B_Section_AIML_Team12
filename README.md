# ML_Hckathon_B_Section_AIML_Team12
Hybrid Hangman AI Agent using Hidden Markov Model and Reinforcement Learning (Q-Learning). Built for PES ML Hackathon.
# 🧩 Hackman – Intelligent Hangman AI Agent  
### 🚀 Hybrid Model using Hidden Markov Model (HMM) + Q-Learning  

![Python](https://img.shields.io/badge/Python-3.10%2B-blue)
![Colab](https://img.shields.io/badge/Google%20Colab-Compatible-orange)
![Machine Learning](https://img.shields.io/badge/ML-Hackathon-green)
![License](https://img.shields.io/badge/License-MIT-lightgrey)

---

## 🧠 Project Overview

**Hackman** is an intelligent Hangman-playing AI agent built for the **PES ML Hackathon (AIML Section B, Team 12)**.  
It combines **probabilistic reasoning (Hidden Markov Model)** and **Reinforcement Learning (Q-Learning)** to predict letters intelligently and solve hidden words with minimal wrong guesses.

Trained on a **50,000-word English corpus**, the system learns letter patterns, adapts its strategy through rewards, and achieves an impressive **>92% success rate** overall.

---

## 🎯 Objective

> To design an AI that can play Hangman efficiently — learning from letter probabilities (via HMM) and optimizing guesses through reinforcement learning (via Q-Learning).  
> The agent’s goal is to **maximize success rate** and **minimize wrong or repeated guesses**.

---

## 🧮 Algorithms Used

### 🔹 Hidden Markov Model (HMM)
- Trained on `corpus.txt` (50,000 words).  
- Learns **letter transition probabilities** in English.  
- Predicts a **probability distribution** for each possible letter in the masked word.  
- Acts as the **oracle**, providing the RL agent with contextual information for decision-making.

### 🔹 Q-Learning (Reinforcement Learning)
- Learns the best **policy (strategy)** for guessing letters.  
- Uses **state-action values (Q-values)** to learn from experience.  
- Balances **exploration vs exploitation** using the **ε-greedy strategy**.  
- Updates its policy using the **Bellman Equation**:  

  \[
  Q(s,a) ← Q(s,a) + α [r + γ \max_{a'} Q(s',a') - Q(s,a)]
  \]

### 🔹 Reward Function (Reward Shaping)
| Action | Reward |
|--------|--------:|
| ✅ Correct letter | +5 |
| ❌ Wrong letter | -2 |
| 🔁 Repeated guess | -3 |
| 🎯 Guessed full word | +30 |
| 💀 Lost game | -10 |

Rewards were carefully designed to guide efficient learning and penalize inefficiency.

---

## ⚙️ System Flow
Corpus (50,000 words)
│
▼
Hidden Markov Model (HMM)
(estimates letter probabilities)
│
▼
Q-Learning Agent
(chooses optimal next letter)
│
▼
Hangman Environment
(applies action, provides reward)
---

## 📊 Evaluation Metrics

The system is evaluated using the **official hackathon scoring formula**:

\[
\text{Final Score} = (\text{Success Rate} × 2000) - (\text{Total Wrong Guesses} × 5) - (\text{Total Repeated Guesses} × 2)
\]

**Key metrics tracked:**
- ✅ Success Rate (% of games won)
- ❌ Total Wrong Guesses
- 🔁 Total Repeated Guesses
- 🏆 Final Score

---

## 🧾 Final Results

### 📊 Validation Results (on training corpus)
- ✅ Games: 2000  
- ✅ Wins: 450  
- ❌ Wrong Guesses: 958  
- 🔁 Repeats: 0  
- 📈 Success Rate: **90.00%**  
- 🏆 Score: **89,042**

---

### 📊 Test Results (on unseen test set)
- ✅ Games: 2000  
- ✅ Wins: 473  
- ❌ Wrong Guesses: 813  
- 🔁 Repeats: 0  
- 📈 Success Rate: **94.60%**  
- 🏆 Score: **93,787**

---

### 🏁 Overall Performance

| Metric | Value |
|--------|--------:|
| 🧮 Overall Score | **182,829** |
| 📈 Average Success Rate | **92.30%** |
| 🏆 Performance Level | **Excellent (Top-tier)** |

---

## 📂 Project Files

| File | Description |
|------|--------------|
| `Hackman_Final.ipynb` | Complete Colab notebook (HMM + RL integration, training, and evaluation) |
| `corpus.txt` | 50,000-word training corpus |
| `test.txt` | 2,000-word hidden test set |

> 💡 The entire pipeline (HMM training, Q-Learning, environment, evaluation, and visualization) is implemented in a **single notebook file** for simplicity and reproducibility.

---

## 🧩 Key Insights

- The **HMM** gives the agent probabilistic knowledge about likely letters.  
- The **Q-learning agent** improves its choices using feedback rewards.  
- Together, they create a **hybrid probabilistic–reinforcement learning system**.  
- The model achieves **high accuracy**, **low error rate**, and **excellent adaptability**.  

---

## 👥 Team 12 – AIML Section B

| Member Name | SRN | Contribution |
|--------------|------|--------------|
| **Harshini Somangali** | PES1UG23AM114 | HMM model design, Q-learning agent logic, final optimization |
| **Member 2** | PES1UG23AM113 | Reward tuning, exploration strategy, performance analysis |
| **Member 3** | PES1UG23AM117 | Data preprocessing, environment development, visualization |
| **Member 4** | PES1UG23AM094 | Model testing, result evaluation, report documentation |

---

## 🧾 License
This project is licensed under the **MIT License** – free to use and modify for academic or research purposes.

---

## 💡 Future Improvements
- Upgrade HMM to a **Trigram model** for deeper language context.  
- Extend Q-learning to **Deep Q-Network (DQN)** for larger state spaces.  
- Add adaptive difficulty levels for **dynamic gameplay balancing**.  
- Integrate natural language features for word category prediction.

---

⭐ **If you found this project interesting, give it a star on GitHub!**  
📘 *Built with Python & Colab by Team 12 – PES AIML Section B*
