# Three-in-One Game Suite
## Watch the Video

[![Video Thumbnail](https://img.youtube.com/vi/VIDEO_ID/hqdefault.jpg)](https://youtu.be/fgp3KH3LsPs?si=f-bQvz6oYE-wYyyx)


## Overview

The **Three-in-One Game Suite** is a Java application project that allows users to play three distinct games from a single launcher:

- **Advanced Sudoku Solver**
- **Tower of Hanoi Visualization**
- **Tic Tac Toe**


## Features

- **Central Launcher**: Easily access and launch any of the three games from a single interface.
- **Stylish GUI**: A modern and responsive interface with 3D buttons for each game.
- **Advanced Algorithms**: Utilizes recursion and backtracking for game logic.

## Getting Started

1. **Clone the Repository**

   ```bash
   git clone https://github.com/chauhansachin13/Three-in-One-Game-Suite.git
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
- 
# 1.Advanced Sudoku Solver

## Overview

**Sudoku** is a popular logic-based number placement puzzle that challenges players to fill a 9x9 grid with digits from 1 to 9.
The grid is divided into nine 3x3 subgrids, called regions or boxes.
The puzzle starts with some cells pre-filled with numbers, and the objective is to complete the grid according to the following rules:

1. **Each row** must contain all digits from 1 to 9 without repetition.
2. **Each column** must contain all digits from 1 to 9 without repetition.
3. **Each 3x3 subgrid** must also contain all digits from 1 to 9 without repetition.

The puzzle is solved when all cells are filled correctly while adhering to these rules.


### Features

- **Sudoku Solver Algorithm**: Implements a backtracking algorithm to efficiently solve Sudoku puzzles.
- **Interactive GUI**: Provides a user-friendly interface to input Sudoku puzzles and view solutions.
- **Color Themes**: Includes five distinct color schemes, each with a unique palette, to customize the appearance of the Sudoku grid.
- **Dynamic Puzzle Generation**: Automatically generates new Sudoku puzzles with varied difficulty levels.
- **Input Validation**: Ensures that only valid numbers (1-9) are entered into the puzzle grid.
- **Customizable Board**: Allows users to reset the board to its initial state or generate a new puzzle.
- **Theme Selection**: Users can switch between predefined themes to enhance visual experience.


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



### Dependencies

- Java Development Kit (JDK) 8 or later

  
# 2.Tower of Hanoi Game

## Overview

The Tower of Hanoi is a classic puzzle where you need to move a stack of disks from one rod to another, following specific rules:

1. Only one disk can be moved at a time.
2. Each move involves taking the top disk from one of the stacks and placing it on top of another stack or an empty rod.
3. No disk may be placed on top of a smaller disk.

## Components

- **Disks and Rods:** The puzzle is represented by three rods and a number of disks of varying sizes.
- **GUI Elements:** The application includes buttons to start solving the puzzle with animation, pause/resume the animation, and reset the game. There is also a slider to control the speed of the animation.

## Working of the Application

### 1. Initialization

When the application starts, it initializes three rods and populates the first rod with disks arranged in descending size order. The disks are colored differently for visual distinction.

### 2. GUI Setup

- **Drawing the Rods and Disks:** The `drawRods` and `drawDisks` methods are used to paint the rods and disks on the panel.
- **Control Panel:** Buttons and a slider are provided to control the animation. The "Solve with Animation" button starts the solving process, the "Pause" button toggles between pausing and resuming, and the "Reset" button resets the game to its initial state. The slider allows adjusting the speed of the animation.

### 3. Solving the Puzzle

The puzzle is solved using a recursive algorithm. Here’s how it works:

- **Recursive Algorithm:** The `generateMoves` method generates the sequence of moves needed to solve the puzzle using recursion.
  - **Base Case:** If there is only one disk, move it directly from the source rod to the destination rod.
  - **Recursive Case:** To move `n` disks from the source rod to the destination rod using an auxiliary rod:
    1. Move `n-1` disks from the source rod to the auxiliary rod.
    2. Move the nth disk (the largest disk) directly to the destination rod.
    3. Move the `n-1` disks from the auxiliary rod to the destination rod.

  This process is repeated until all disks are moved to the destination rod in the correct order.

### 4. Animation

- **Timer for Animation:** A `Timer` object controls the animation speed. It triggers moves at intervals specified by the slider.
- **Performing Moves:** The `performMove` method is called to move disks according to the sequence generated by the recursive algorithm. The panel is repainted after each move to update the visual representation.
- **Adjusting Speed:** The slider’s value determines the delay between moves, affecting the animation speed. Moving the slider adjusts the timer’s delay.

### 5. Pause/Resume

- **Pause Functionality:** Clicking the "Pause" button stops the timer, halting the animation. Clicking it again resumes the animation by restarting the timer.
- **State Management:** A flag (`isPaused`) is used to track whether the animation is currently paused.

### 6. Reset

- **Resetting the Game:** The `resetGame` method clears all disks from the rods, reinitializes the first rod with disks, and resets the animation state.

## Code Walkthrough

1. **`TowerOfHanoiGUI` Class:**
   - Initializes the GUI components and handles user interactions.
   - Implements methods to draw the rods and disks, solve the puzzle, and manage animation.

2. **`Disk` Class:**
   - Represents a disk with a color and size.

3. **`Rod` Class:**
   - Represents a rod with a stack of disks.

4. **`Move` Class:**
   - Represents a move from one rod to another.

5. **`generateMoves` Method:**
   - Generates the sequence of moves required to solve the puzzle using recursion.

6. **`performMove` Method:**
   - Moves disks between rods and updates the visual representation.

7. **`adjustTimerSpeed` Method:**
   - Adjusts the animation speed based on the slider value.

# 3.Tic-Tac-Toe Game

## Overview

The Tic-Tac-Toe game is a classic two-player game where players take turns to mark spaces on a 3x3 grid. The goal is to get three of your marks (either 'X' or 'O') in a row—either horizontally, vertically, or diagonally—before your opponent does. This project is a graphical implementation of Tic-Tac-Toe using Java Swing.

## Features

- **Graphical User Interface (GUI):** A visually appealing board with buttons for each cell.
- **Player Turns:** Players alternate between 'X' and 'O'.
- **Winning Detection:** Automatically detects and announces the winner.
- **Draw Detection:** Detects if the game ends in a draw.
- **Animation:** Brief animation effect when a player makes a move.
- **Reset Functionality:** Resets the board after a win or draw.

## How It Works

### 1. **Initialization**

When the game starts, a 3x3 grid of buttons is created to represent the board. Each button can be clicked to make a move. The application initializes with player 'X' starting the game.

### 2. **User Interaction**

- **Making a Move:** Clicking a button places the current player's mark ('X' or 'O') in that cell. The button is then animated to provide visual feedback.
- **Switching Turns:** After a move, the current player switches to the other player.

### 3. **Checking for a Winner**

The game checks for a win or draw after each move:
- **Win Condition:** A player wins if they have three of their marks in a row, either horizontally, vertically, or diagonally.
- **Draw Condition:** If all cells are filled and no player has won, the game ends in a draw.

### 4. **Animating Moves**

When a move is made, the button is briefly highlighted with a color animation to indicate the action.

### 5. **Resetting the Game**

After a win or draw, a message is shown, and the board is reset for a new game.

## Code Overview

Here is a skeleton of the main components and methods in the `TicTacToe` class:

```java
import javax.imageio.ImageIO;
import javax.swing.*;
import java.awt.*;
import java.awt.event.ActionEvent;
import java.awt.event.ActionListener;
import java.io.File;
import java.io.IOException;

public class TicTacToe extends JFrame implements ActionListener {
    private static final int SIZE = 3;
    private JButton[][] buttons;
    private char currentPlayer;
    private JPanel boardPanel;

    public TicTacToe() {
        // Constructor to initialize the game
    }

    private void initializeBoard() {
        // Initializes the 3x3 board with buttons
    }

    private void animateMove(JButton button) {
        // Animates the button to provide visual feedback
    }

    private void updateButtonStyle(JButton button) {
        // Updates the style of the button
    }

    private void makeMove(JButton button) {
        // Handles the move and updates the game status
    }

    private boolean checkWin() {
        // Checks if the current player has won
        return false;
    }

    private boolean isBoardFull() {
        // Checks if the board is full
        return false;
    }

    private void resetBoard() {
        // Resets the board for a new game
    }

    @Override
    public void actionPerformed(ActionEvent e) {
        // Handles button click events
    }

    public static void main(String[] args) {
        SwingUtilities.invokeLater(() -> new TicTacToe());
    }
}
```

### Key Methods

- **`initializeBoard()`**: Sets up the 3x3 grid with buttons.
- **`animateMove(JButton button)`**: Provides visual feedback when a move is made.
- **`updateButtonStyle(JButton button)`**: Styles the buttons for a clean appearance.
- **`makeMove(JButton button)`**: Executes a move and checks for win or draw.
- **`checkWin()`**: Determines if the current player has won.
- **`isBoardFull()`**: Checks if the board is fully occupied.
- **`resetBoard()`**: Resets the board for a new game.

---

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

## Dependencies

- Java Development Kit (JDK) 8 or later

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Acknowledgements

- Developed solo by **Sachin Chauhan**.
```

