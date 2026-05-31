# Epidemic Restriction Optimizer — PSO

A Particle Swarm Optimization model that finds the optimal restriction policy across city zones to minimize both infection spread and economic cost.

## Problem
Given 8 city zones with different populations, risk levels, and economic values — find the restriction level (0–100%) for each zone that balances:
- Minimizing infections (SIR-based attack rate model)
- Minimizing economic disruption

## How it works
Each particle represents a policy (one restriction value per zone).
The swarm minimizes a fitness function:

fitness = 0.5 × (infections / max_infections) + 0.5 × (cost / max_cost)

Converges early if no improvement is found for 40 consecutive iterations.

## Tech Stack
Python (no external dependencies)

## Run
Open `epidemic-control.ipynb` in Jupyter or VS Code and run all cells.

## Sample Output
```
ZONE               | ORIGINAL POP |   RESTR. |   INFECTED |  ECON COST
---------------------------------------------------------------------------
City Center        |       10,000 |   73.3% |        200 |    1100000
North District     |        8,000 |   60.0% |        160 |     480000
...
Final Best Fitness: 0.329397
```
