![Team Banner](/images/Team%20Banner.png)

# RoboCup Software Team Recruitment Tasks 2026-27

## Welcome to the recruitment process for the RoboCup Humainoid Kid's sized league Software team! This repository contains two tasks designed to evaluate your understanding of computer vision, machine learning, and data processing in the context of robotic soccer.

## Task 1: Djikstra vs Greedy Best First Search path finding algorithm
Use this single 10x10 grid for all parts of the task. Represent it as a 2D list or NumPy array.
```
python
# 0=Empty, 1=Shelf (obstacle), 2=Robot, 3=Package
grid = [
    [0, 0, 0, 1, 0, 0, 0, 1, 0, 0],
    [0, 1, 0, 1, 0, 1, 0, 1, 0, 0],
    [0, 1, 0, 0, 0, 1, 0, 0, 0, 0],
    [0, 1, 0, 0, 0, 1, 0, 0, 1, 0],
    [0, 0, 0, 1, 0, 0, 0, 0, 1, 0],
    [0, 0, 0, 1, 0, 0, 1, 0, 1, 0],
    [0, 0, 0, 1, 0, 0, 1, 0, 0, 0],
    [1, 1, 0, 0, 0, 0, 1, 0, 0, 0],
    [0, 0, 0, 0, 1, 0, 0, 0, 1, 0],
    [0, 2, 0, 0, 0, 0, 0, 0, 3, 0],
]
start_pos = (9, 1)   # Robot starts bottom-left area
goal_pos  = (9, 8)   # Package is bottom-right area
Create your own grid (keeping the same legend) and use it throughout.
```
## 1.2 Implement Algorithms

Implement **two functions**, each accepting the grid, a start position, and a goal position as inputs. The robot may move **Up, Down, Left, and Right** only (no diagonals).

### Algorithm 1 — Dijkstra's Algorithm
A cost-based search that finds the lowest-cost path. Treat every move as having a uniform cost of 1 (equivalent to BFS on an unweighted grid), but structure your implementation using a **priority queue** keyed on cumulative cost. This prepares it for weighted grids in Part 1.3.

### Algorithm 2 — Greedy Best-First Search
A heuristic-driven algorithm that always expands the node that *looks* closest to the goal, without tracking actual path cost. Use **Manhattan Distance** as the heuristic:

h = |row1 - row2| + |col1 - col2|
Each function must return:
•	The final path — an ordered list of (row, col) coordinates from start to goal (inclusive)
•	The number of nodes explored during the search

## Task 2: Ball Detection Dataset & Model Training
### Overview
In this task, you will:
- **Create a Ball Detection Dataset**
  - Use Roboflow to build your own dataset for ball detection
  - Limited to 20 images maximum
  - Focus on understanding the basics of dataset creation
- **Train a Detection Model**
  - Train your model using free GPU resources (Kaggle or Google Colab)
  - Optionally incorporate open source datasets
  - Extra points for well-curated datasets
### Deliverables
- Trained model file (`.pt`, `.pth`, `.bin`, `.onnx`, `.t5`, or other standard format)
- Screenshot of your Roboflow dataset
- Link to any open source dataset used (if applicable)
- Brief explanation of your methodology and approach

## Notes

- We prioritize methodology and clear understanding over complex analysis
- Focus on communicating your findings effectively
- Show your ability to extract meaningful insights from sports data
- You don't need to analyze the entire database - choose specific aspects that interest you
- Time management is important - complete the basic requirements before attempting optional tasks

Good luck with your submission! If you have any questions, please reach out through the appropriate channels.
