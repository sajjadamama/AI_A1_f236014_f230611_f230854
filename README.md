# Pathfinding Visualizer

An interactive pathfinding visualizer built with **Pygame** that animates six classic search algorithms on a live, editable grid — complete with dynamic obstacles that spawn mid-search.

---

## Features

- **Six algorithms** visualized in real time: BFS, DFS, DLS, IDDFS, UCS, and Bidirectional Search
- **Click-to-build** interface — place your start, target, and wall obstacles with a mouse
- **Dynamic obstacles** that randomly appear during search, simulating real-world path disruption
- **Animated path reconstruction** once the target is found
- **Instant reset** to try a new scenario without restarting the program

---

## Algorithms

| Key | Algorithm | Strategy | Optimal? |
|-----|-----------|----------|----------|
| `Space` | **BFS** (Breadth-First Search) | Explores layer by layer | Yes (uniform cost) |
| `D` | **DFS** (Depth-First Search) | Dives deep before backtracking |  No |
| `L` | **DLS** (Depth-Limited Search) | DFS with a depth cap of 10 | No |
| `I` | **IDDFS** (Iterative Deepening DFS) | Repeating DLS with increasing depth |  Yes |
| `U` | **UCS** (Uniform-Cost Search) | Expands lowest-cost node first |  Yes |
| `B` | **Bidirectional Search** | Searches simultaneously from both ends |  Yes |

---

##  Color Legend

| Color | Meaning |
|-------|---------|
| 🟩 Green | Start node |
| 🟥 Red | Target node |
| ⬛ Grey | Wall / obstacle |
| 🟨 Yellow | Visited node (forward frontier) |
| 🩵 Cyan | Visited node (backward frontier / DLS) |
| 🟦 Blue | Final path |

---

##  Getting Started

### Prerequisites

```bash
pip install pygame
```

### Run

```bash
python pathfinding_visualizer.py
```

---

##  How to Use

1. **Left-click** on an empty cell to place the **start node** (green)
2. **Left-click** again to place the **target node** (red)
3. **Left-click** any other cell to draw **walls** (grey)
4. Press one of the algorithm keys to **start the search**
5. Press `C` to **clear the grid** and start fresh

> **Tip:** Walls can be placed before or after setting start/target. Build a maze, then watch each algorithm navigate it differently!

---

##  Keyboard Shortcuts

| Key | Action |
|-----|--------|
| `Space` | Run BFS |
| `D` | Run DFS |
| `L` | Run DLS (depth limit: 10) |
| `I` | Run IDDFS (max depth: 15) |
| `U` | Run UCS |
| `B` | Run Bidirectional Search |
| `C` | Clear grid and reset |

---

##  Configuration

These constants at the top of the file can be tweaked to customize behavior:

```python
ROWS = 10                   # Grid dimensions (ROWS × ROWS)
DYNAMIC_PROBABILITY = 0.02  # Chance per step of a new obstacle spawning
```

Increasing `ROWS` gives a larger, more detailed grid. Increasing `DYNAMIC_PROBABILITY` makes the environment more chaotic and tests algorithm resilience.

---

## Movement

The visualizer supports **8-directional movement** (including diagonals), so paths can cut corners for more natural routing.

---

## Project Structure

```
pathfinding_visualizer.py   # Single-file application — everything lives here
```

---

##  License

free to use, modify, and share.
