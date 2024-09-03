Here is the complete content for the `README.md` file, formatted as a single code block:


# Three-in-One Game Suite

## Overview

The **Three-in-One Game Suite** is a Java application project developed entirely by me. It allows users to play three distinct games from a single launcher:

- **Advanced Sudoku Solver**: Solve and visualize Sudoku puzzles.
- **Tower of Hanoi Visualization**: Interactive and animated Tower of Hanoi puzzle.
- **Tic Tac Toe**: A classic Tic Tac Toe game with visual feedback.

The application features a user-friendly graphical interface (GUI) and utilizes recursion and backtracking algorithms in the backend to power the games.

## Features

- **Central Launcher**: Easily access and launch any of the three games from a single interface.
- **Stylish GUI**: A modern and responsive interface with 3D buttons for each game.
- **Advanced Algorithms**: Utilizes recursion and backtracking for game logic.

## Getting Started

1. **Clone the Repository**

   ```bash
   git cloneh https://github.com/chauhansachin13/Three-in-One-Game-Suite.git
   ```

2. **Navigate to the Project Directory**

   ```bash
   cd three-in-one-game-suite
   ```

3. **Compile the Java Files**

   ```bash
   javac GameLauncherGUI.java SudokuSolverGUI.java TowerOfHanoiGUI.java TicTacToe.java
   ```

4. **Run the Game Launcher**

   ```bash
   java GameLauncherGUI
   ```

## Project Structure

- `GameLauncherGUI.java`: Main launcher class that provides access to all three games.
- `SudokuSolverGUI.java`: GUI for the Advanced Sudoku Solver.
- `TowerOfHanoiGUI.java`: GUI for the Tower of Hanoi Visualization.
- `TicTacToe.java`: GUI for the Tic Tac Toe game.

- Certainly! Here’s a more detailed and descriptive `README.md` for the **Advanced Sudoku Solver** sub-project:


## Advanced Sudoku Solver

### Overview

The **Advanced Sudoku Solver** is a comprehensive Java application designed to solve Sudoku puzzles with enhanced user interaction and customization features. It combines a powerful Sudoku-solving algorithm with a dynamic graphical user interface (GUI) that includes multiple color themes and interactive elements. This project demonstrates the integration of algorithms with user-centric design, providing both functionality and visual appeal.

### Features

- **Sudoku Solver Algorithm**: Implements a backtracking algorithm to efficiently solve Sudoku puzzles.
- **Interactive GUI**: Provides a user-friendly interface to input Sudoku puzzles and view solutions.
- **Color Themes**: Includes five distinct color schemes, each with a unique palette, to customize the appearance of the Sudoku grid.
- **Dynamic Puzzle Generation**: Automatically generates new Sudoku puzzles with varied difficulty levels.
- **Input Validation**: Ensures that only valid numbers (1-9) are entered into the puzzle grid.
- **Customizable Board**: Allows users to reset the board to its initial state or generate a new puzzle.
- **Theme Selection**: Users can switch between predefined themes to enhance visual experience.

### Installation

1. **Ensure Java Development Kit (JDK) is installed**: This project requires JDK 8 or later.
2. **Compile the Source Code**:

   ```bash
   javac SudokuSolverGUI.java
   ```

3. **Run the Application**:

   ```bash
   java SudokuSolverGUI
   ```

### User Interface

Upon running the application, a window will appear with the following components:

- **Sudoku Grid**: A 9x9 grid representing the Sudoku puzzle. Each cell can be filled with numbers between 1 and 9.
- **Buttons**:
  - **Solve**: Attempts to solve the current Sudoku puzzle and displays the solution in the grid.
  - **Reset**: Restores the grid to its initial state.
  - **Re-Generate**: Generates a new Sudoku puzzle with a fresh layout and updates the grid.
  - **Change Theme**: Cycles through different color themes to modify the appearance of the grid.
- **Menu Bar**:
  - **Select Theme**: Allows users to select from five different themes via a dropdown menu.

### Code Explanation

#### SudokuSolver Class

This class contains the logic for solving Sudoku puzzles using a backtracking approach. It ensures that each number placed in the grid adheres to Sudoku rules, which are:
- Each number from 1 to 9 must appear exactly once in each row.
- Each number must appear exactly once in each column.
- Each number must appear exactly once in each 3x3 subgrid.

```java
class SudokuSolver {
    public boolean solveSudoku(int[][] board) {
        return solve(board);
    }

    private boolean solve(int[][] board) {
        // Recursive method to solve the Sudoku board
    }

    private boolean isValid(int[][] board, int row, int col, int num) {
        // Checks if placing a number in the given position is valid
    }
}
```

#### SudokuSolverGUI Class

This class manages the graphical interface and user interactions. It initializes the GUI components, handles user inputs, updates the grid based on actions, and applies color themes.

```java
public class SudokuSolverGUI {
    private JFrame frame;
    private JTextField[][] cells;
    private SudokuSolver solver;
    private int[][] initialBoard;
    private Color[][] themes;
    private int currentThemeIndex;

    public SudokuSolverGUI() {
        // Set up the GUI, initialize components, and configure event listeners
    }

    private void initializeBoard() {
        // Generates a new Sudoku puzzle and updates the GUI
    }

    private void restoreInitialBoard() {
        // Resets the grid to its initial state
    }

    private void generateFullSudokuBoard(int[][] board) {
        // Creates a complete Sudoku board and solves it
    }

    private void updateColors() {
        // Updates the cell colors based on the selected theme
    }

    public static void main(String[] args) {
        SwingUtilities.invokeLater(SudokuSolverGUI::new);
    }
}
```

#### JTextFieldLimit Class

This class restricts user input in the grid cells to a single digit between 1 and 9.

```java
class JTextFieldLimit extends javax.swing.text.PlainDocument {
    private int limit;

    JTextFieldLimit(int limit) {
        super();
        this.limit = limit;
    }

    @Override
    public void insertString(int offset, String str, javax.swing.text.AttributeSet attr)
            throws javax.swing.text.BadLocationException {
        // Validates input to ensure it is a single digit between 1 and 9
    }
}
```

### Screenshots

*(Include screenshots here to illustrate the application's appearance and functionality)*

### Dependencies

- Java Development Kit (JDK) 8 or later

### License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.

### Acknowledgements

- Developed and maintained by [Your Name].
- Special thanks to resources and libraries that facilitated the development of this project.

---

Feel free to update placeholders with your personal details and add any additional information or images as needed.
```

This README provides a comprehensive overview of the project, including its features, code details, and usage instructions. Adjust the content as needed to fit your specific requirements and preferences.

## Dependencies

- Java Development Kit (JDK) 8 or later

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Acknowledgements

- Developed solo by [Your Name].
```

You can replace `[Your Name]` with your actual name and adjust the URL in the `git clone` command to match your repository.
