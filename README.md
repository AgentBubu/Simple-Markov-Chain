# Markov Chain Weather Simulation

This project simulates weather patterns using a Markov chain model, focusing on two possible weather states: **sunny** and **rainy**. The simulation estimates weather transition probabilities and generates a realistic sequence of weather based on these probabilities.

## Features

- Simulates a sequence of weather states (sunny/rainy) over a specified number of days.
- Calculates and prints the number of sunny and rainy days in the simulation.
- Computes the steady-state distribution of the Markov chain mathematically.
- Includes both an original implementation using the Pomegranate library and a NumPy-based version for environments where Pomegranate is unavailable.

## How It Works

- **States:** `sun`, `rain`
- **Initial Probabilities:** 50% chance for each state.
- **Transition Matrix:**
  - If today is sunny: 80% chance of sun tomorrow, 20% chance of rain.
  - If today is rainy: 30% chance of sun tomorrow, 70% chance of rain.

The simulation randomly generates a sequence of weather states based on these probabilities and transition rules.

## Usage

Open and run the notebook [`MarkovChain.ipynb`](MarkovChain.ipynb) in Jupyter or VS Code. The notebook contains:

- The original code using Pomegranate.
- A modified version using NumPy (no external dependencies except NumPy).
- Explanations and analysis of the model and results.

## Example Output

```
['rain', 'rain', 'rain', ..., 'sun', 'rain']
Number of sunny days: 28
Number of rainy days: 22

Steady state calculation:
Step 1: [0.55 0.45] | Δ = 0.050000
...
✅ Steady state reached at step 10: [0.599902 0.400098]
```

## Requirements

- Python 3.x
- NumPy

## References

- [Original inspiration from Github Ravissement](https://github.com/ravissement/MarkovChain)

---

**Author:** Elisabeth Victoria Nilasari
