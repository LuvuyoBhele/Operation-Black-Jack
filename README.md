# 🃏 Blackjack Game & Simulation (Python)

## 📖 Overview
This project contains two components:  
1. **Interactive Blackjack Game** – Play against the dealer in the console.  
2. **Blackjack Simulation** – Run thousands of automated games to analyze strategies and outcomes, with results exported to Excel for further study.  

It’s a simplified version of Blackjack using numbers only (`2–10`, face cards as `10`, Ace as `11` with automatic downgrade to `1` when needed).


## 🚀 Features
- **Interactive Mode**:
  - User vs dealer gameplay with `hit` or `stay` decisions.
  - Dealer logic: draws until reaching at least 13.
  - Win/lose/tie conditions with replay option.
- **Simulation Mode**:
  - Run large numbers of games (`n=10,000` or more).
  - Strategy parameter (`safeHit`) defines when the user should stop hitting.
  - Results stored in a Pandas DataFrame.
  - Export outcomes to Excel for analysis.

## 🛠️ Requirements
- Python 3.7 or higher  
- Libraries:
  - `random` (built-in)
  - `numpy`
  - `pandas` (for DataFrame and Excel export)

## ▶️ How to Run

### Interactive Game
```bash
python blackjack.py
```

### Simulation
```bash
python blackjack_sim.py
```

Example:
```python
df = black_jack_sim(10000, 21)
print(df)
df.to_excel("results.xlsx", index=False, sheet_name="threshold_hit_21")
```

## 🎮 Gameplay Instructions
- **Interactive Mode**:
  - Start with two cards.
  - Choose to **Hit (h)** or **Stay (s)**.
  - Dealer plays after you stay.
  - Win if closer to 21 than dealer, lose if you bust or dealer wins, tie if equal.
- **Simulation Mode**:
  - Automated play using `hitOrStay()` strategy.
  - Results classified as `win`, `lose`, or `push`.


## 📂 Project Structure
```
blackjack-project/
│── blackjack.py        # Interactive game
│── blackjack_sim.py    # Simulation script
│── README.md           # Documentation
│── results.xlsx        # Example output (optional)
```


## ✨ Future Improvements
- Refine dealer strategy (e.g., hit until 17 instead of 21).
- Add betting system with chips/money.
- Track win/loss ratios across different `safeHit` thresholds.
- Use a full deck with suits and face cards.
- Visualize simulation results with charts.


## 🤝 Contributing
Pull requests are welcome! Fork the repo and submit a PR if you’d like to improve the game logic or add new features.
