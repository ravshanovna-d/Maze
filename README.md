<div align="center">

# 🧩 Maze Solver: Graphs & Q-Learning

**Generating mazes, finding paths with graph search and teaching an agent to escape with reinforcement learning.**

![Python](https://img.shields.io/badge/Python-3.11-3776AB?logo=python&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-grid-013243?logo=numpy&logoColor=white)
![NetworkX](https://img.shields.io/badge/NetworkX-graphs-2C7BB6)
![Matplotlib](https://img.shields.io/badge/Matplotlib-visualization-11557C)
![RL](https://img.shields.io/badge/Reinforcement%20Learning-Q--learning-8A2BE2)

</div>

---

## 📌 Overview

An interactive Jupyter notebook that explores the same problem, getting from **S**tart to **G**oal, in three ways:

1. **Modeling**: a maze is a NumPy grid (`0` = free cell, `1` = wall), drawn with Matplotlib
2. **Graph search**: a random maze is generated, turned into a **NetworkX graph** and solved with the **shortest path**
3. **Reinforcement learning**: a `MazeGame` environment (`reset` / `step`) where an agent learns a policy with a **Q-table**

## ✨ What's Inside

| Part | Description |
|---|---|
| `Maze` class | Stores the layout, start and goal, renders the maze |
| Maze generation | Randomized **depth-first search** (recursive backtracker) carves a perfect maze |
| Graph solver | Converts the carved edges to a graph and solves with `nx.shortest_path`, path is drawn over the maze |
| Step maze | A staircase-shaped maze to test agents on a known optimal route |
| `MazeGame` env | Gym-like environment with actions, rewards and terminal state |
| Q-learning agent | Learns action values in a Q-table, prints steps and total reward |
| Widgets | `ipywidgets.interact` to change maze parameters live |

## 🚀 Getting Started

```bash
git clone https://github.com/ravshanovna-d/Maze.git
cd Maze
pip install numpy matplotlib networkx ipywidgets jupyter
jupyter notebook Maze.ipynb
```

Or open `Maze.ipynb` directly in [Google Colab](https://colab.research.google.com/).

## 🧠 Concepts Practiced

- Grid and graph representations of a search space
- DFS maze generation and shortest-path search
- Markov Decision Process: states, actions, rewards
- Q-learning and exploration vs. exploitation

## 🗺 Roadmap

- [ ] Compare BFS, A* and Dijkstra on the same maze
- [ ] Animate the agent's learned path
- [ ] Plot the reward per episode learning curve
