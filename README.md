# N-Queens Puzzle Solver

A clean and efficient implementation of the classic **N-Queens Puzzle**, demonstrating algorithmic problem-solving, recursion, and constraint satisfaction.

## Overview

The **N-Queens Puzzle** is a foundational computer science and combinatorial optimization problem. The objective is to place N chess queens on an N × N chessboard such that no two queens threaten each other. According to standard chess rules, no two queens may share the same row, column, or diagonal.

This repository provides a scalable solver capable of computing valid board configurations for arbitrary board sizes (N ≥ 1).

## Algorithm & Complexity

This implementation utilizes a **Recursive Backtracking** approach (with branch pruning) to explore the state space efficiently:
1. Queens are placed sequentially row by row.
2. Before placing a queen at `(row, col)`, the algorithm validates that the column and both diagonals are safe from existing queens.
3. If a conflict occurs or a dead end is reached, the algorithm backtracks to the previous row and explores the next available column.

* **Time Complexity:** \(\mathcal{O}(N!)\) — Significant pruning reduces the search space compared to a brute-force \(\mathcal{O}(N^N)\) approach.
* **Space Complexity:** \(\mathcal{O}(N^2)\) to store the board state (or \(\mathcal{O}(N)\) auxiliary stack/tracking space).

## Features

- **Configurable Board Size:** Supports any positive integer N.
- **Complete Solution Enumeration:** Finds all distinct valid board configurations (e.g., 2 solutions for N=4, 92 solutions for N=8).
- **Visual Board Output:** Renders clean, human-readable ASCII representations of valid boards.

## Getting Started

### Prerequisites
- [Specify Language & Version, e.g., Python 3.8+ / GCC 11+ / Node.js 18+]

### Installation & Usage

1. **Clone the repository:**
   ```bash
   git clone https://github.com
   cd n-queens-solver
   ```

2. **Run the solver:**
   ```bash
   # Replace with your actual execution command
   python main.py --n 4
   ```

### Sample Output (N = 4)

```text
Total distinct solutions found: 2

Solution 1:
. Q . .
. . . Q
Q . . .
. . Q .

Solution 2:
. . Q .
Q . . .
. . . Q
. Q . .
```

## Contributing

Contributions, optimizations (such as bitwise state tracking or iterative approaches), and bug reports are welcome. Feel free to open an issue or submit a pull request.

## License

This project is licensed under the MIT License — see the [LICENSE](LICENSE) file for details.
