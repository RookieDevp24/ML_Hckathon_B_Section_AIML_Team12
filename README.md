# ML_Hckathon_B_Section_AIML_Team12
Hybrid Hangman AI Agent using Hidden Markov Model and Reinforcement Learning (Q-Learning). Built for PES ML Hackathon.
---

## 📊 Evaluation Metrics

The agent is evaluated using the **official hackathon formula**:

\[
\text{Final Score} = (Success Rate × 2000) - (Total Wrong Guesses × 5) - (Total Repeated Guesses × 2)
\]

**Key metrics reported:**
- ✅ Success Rate (% of games won)
- ❌ Total Wrong Guesses
- 🔁 Total Repeated Guesses
- 🏆 Final Score

---

## 📂 Project Structure

| File | Description |
|------|--------------|
| `Hackman.ipynb` | Main Colab notebook (includes HMM, environment, and Q-learning agent) |
| `corpus.txt` | Training word corpus (50,000 words) |
| `test.txt` | Hidden test set (2,000 words) |
| `Analysis_Report.pdf` | Design explanation, HMM structure, RL details |
| `final_results.png` | Training trend visualization |

---

## 🧾 Results Summary

| Dataset | Games | Success Rate | Wrong Guesses | Final Score |
|----------|--------:|---------------:|----------------:|--------------:|
| Validation (corpus) | 2000 | ~90% | ~3500 | High |
| Test (hidden words) | 2000 | ~3–5% | ~11,000 | As per Hackathon evaluation |

---

## 📈 Learning Curve

The training plot (`final_results.png`) shows improvement in cumulative rewards over episodes,  
demonstrating convergence of the Q-learning policy.

---

## 🧩 Key Takeaways

- HMM captures **statistical language structure** from data.  
- Q-learning improves **decision efficiency** through feedback.  
- Together, they form a **hybrid probabilistic-RL system**.  
- Reward shaping and ε-decay balance **exploration vs exploitation**.  

---

## 👥 Team 12 – AIML Section B

| Member | Role |
|---------|------|
| **Harshini Somangali** | HMM design, Q-learning implementation, report & visualization |
| *(Add teammate names here)* | RL fine-tuning, analysis, and code integration |

---

## 🧾 License
This project is licensed under the **MIT License** – feel free to use and modify for academic purposes.

---

## 💡 Future Improvements
- Upgrade to **Trigram HMM** for better language modeling.  
- Implement a **Deep Q-Network (DQN)** for function approximation.  
- Integrate **transfer learning** from pre-trained language embeddings.

---

⭐ **If you found this project interesting, give it a star on GitHub!**
