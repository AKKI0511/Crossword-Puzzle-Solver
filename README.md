# Crossword Puzzle Solver

This Python project implements a solver for a maze-like puzzle using a search algorithm. The solver navigates through a maze represented in a text file, finds a path from the start point to the goal point, and visualizes the solution.

## Usage

1. Clone the repository:

   ```bash
   git clone https://github.com/AKKI0511/Crossword-Puzzle-Solver.git
   cd crossword-puzzle-solver
   ```

2. Run the solver:

   ```bash
   python maze.py maze.txt
   ```

   Replace `maze.txt` with the path to your maze file.

## Maze File Format

The maze file should contain the maze layout using the following symbols:

- `"A"`: Start point.
- `"B"`: Goal point.
- `" "` (space): Empty cell.
- `"█"`: Wall.

Example maze file (`maze.txt`):

```
█████B█████
█A   █   ██
█ ███ █ ███
█     █   ██
███████████
```

## Classes

### `Node`

- Represents a state in the search space.
- Contains information about the state, its parent, and the action that led to it.

### `StackFrontier` and `QueueFrontier`

- Implement frontier data structures (stack and queue) for managing nodes during search.
- Support operations like adding, removing, checking containment, and checking emptiness.

### `Maze`

- Represents the maze puzzle.
- Reads the maze layout from a file, initializes the maze, and provides methods for solving and visualizing the maze.
- Uses a search algorithm to find a path from the start to the goal.

## Functions

- `solve()`: Finds a solution to the maze using a search algorithm.
- `print()`: Prints the maze layout with the solution path.
- `output_image()`: Generates and saves an image representation of the maze with the solution path and explored cells.

## Dependencies

- Python 3
- PIL (Python Imaging Library)

Install PIL using pip:

```bash
pip install Pillow
```

## Output

After running the solver, it will print:

- The maze layout.
- The number of states explored during the search.
- The maze layout with the solution path marked.

It will also save an image (`maze.png`) of the maze with the explored cells highlighted if you pass `show_explored=True` to the `output_image()` method.

`maze.png`:

![image](https://github.com/AKKI0511/Crossword-Puzzle-Solver/assets/120317569/0fd7e193-d098-4226-ba7b-685c41e336d6)
