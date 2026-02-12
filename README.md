# t20-worldcup-montecarlo-predictor
This project predicts the winner of the T20 Cricket World Cup using a **Monte Carlo Simulation** approach combined with an **ELO-based rating system** to estimate match win probabilities.

# 🏏 T20 World Cup Winner Prediction using Monte Carlo Simulation

The model simulates the entire tournament thousands of times to estimate each team's probability of winning the World Cup.

---

## 📌 Project Overview

Cricket matches, especially T20 format, are highly unpredictable.  
This project applies:

- 📊 **ELO Rating System** – To calculate relative team strengths  
- 🎲 **Monte Carlo Simulation** – To simulate the tournament multiple times  
- 📈 Probability Modeling – To estimate win probabilities  

By running large-scale simulations, we approximate the likelihood of each team winning the tournament.

---

## ⚙️ Methodology

### 1️⃣ ELO Rating System
- Each team is assigned an initial rating.
- Match outcomes update ratings dynamically.
- Winning probability is calculated using:

$$
P(A) = \frac{1}{1 + 10^{(R_B - R_A)/100}}
$$

The choice of value of 100 is choosen so that the winning probability among the teams looks natural. (Original value is 400) 

Where:
- $R_A$ = Rating of Team A  
- $R_B$ = Rating of Team B  

---

### 2️⃣ Monte Carlo Simulation

- Simulate each match using calculated win probabilities.
- Run the full tournament simulation **N times** (e.g., 10,000 iterations).

Final winning probability:

$$
\text{Winning Probability} = \frac{\text{Number of Tournament Wins}}{\text{Total Simulations}}
$$

---

## 🛠 Tech Stack

- **Python 3**
- NumPy
- Pandas
- Random module
- Matplotlib (optional for visualization)

---


