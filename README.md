# 🧬 Laboratory n° 2 — Computational Intelligence

## Overview

This laboratory focuses on solving the **Traveling Salesman Problem (TSP)** using techniques from **Evolutionary Computation (EC)**.  
The goal is to find the shortest possible route that visits each city exactly once and returns to the starting point.

The `tsp.ipynb` notebook implements a complete **evolutionary algorithm**, including fitness evaluation, mutation and recombination operators, and various validation tests.

---

## Project Structure

The notebook is organized into several sections, each responsible for a key component of the evolutionary approach:

- **Mutation functions**  
  Implement different mutation strategies (`inversion`, `swap`, `insertion`, `shuffle`, `three_opt`) and test which performs best for each problem type.

- **Recombination functions**  
  Combine genetic material from two parents (e.g., *Cycle Crossover*, *PMX*) to generate new valid tours while preserving genetic diversity.

- **Mutation testing**  
  Includes an experimental section where the performance of each mutation operator is tested to identify which is most effective for a given TSP instance.

- **Parent selection function**  
  Implements selection mechanisms to choose the best individuals for reproduction, balancing exploration and exploitation.

- **Genetic algorithm**  
  The main loop that brings together all components: initialization, selection, crossover, mutation, and evaluation of the new population.

---

## Results

The results obtained in the notebook demonstrate the effectiveness of evolutionary methods for TSP optimization:

- The algorithm achieved **consistent convergence** across multiple problem instances.  
- The **mutation operator** proved crucial for performance:
  - `inversion` was the most effective for structured “g” problems, yielding stable and balanced tours.  
  - `three_opt` outperformed others on “r1” and “r2” problems, thanks to its strong local refinement capabilities.  
- **Recombination operators** improved population diversity, helping to avoid premature convergence and stagnation,
   but **mutation** remains the most defining mechanism for the final quality of the solution.





