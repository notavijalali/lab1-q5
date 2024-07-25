# lab1-q5

Sudoku Class and Methods
Data Members:

grid[9][9]: Stores the Sudoku grid.
solnGrid[9][9]: Stores the solution of the Sudoku grid.
guessNum[9]: Stores numbers for guessing and filling the grid.
gridPos[81]: Stores positions for shuffling and generating puzzles.
difficultyLevel: Represents the difficulty level of the Sudoku puzzle.
grid_status: Indicates the validity of the Sudoku grid.
Constants:

UNASSIGNED: Defined constant (typically 0) representing empty cells in the grid.
Member Functions:

getGrid(): Returns the current Sudoku grid as a string in row-major order.

genRandNum(int maxLimit): Generates a random number between 0 and maxLimit.

Helper Functions for Solving:

FindUnassignedLocation(): Finds an empty cell in the Sudoku grid.
UsedInRow(), UsedInCol(), UsedInBox(): Check if a number is already used in a row, column, or 3x3 box.
isSafe(): Checks if placing a number at a specific position is safe according to Sudoku rules.
fillEmptyDiagonalBox(int idx): Fills the diagonal boxes with random numbers.

createSeed(): Creates a Sudoku seed by filling diagonal boxes and solving the grid to ensure uniqueness.

Sudoku() and Sudoku(string grid_str, bool row_major): Constructors for initializing a Sudoku object. The second constructor allows initialization from a string representation of the grid.

verifyGridStatus(): Verifies the validity of the Sudoku grid.

printGrid(): Prints the current Sudoku grid.

solveGrid(): Solves the Sudoku grid recursively using backtracking.

countSoln(int &number): Counts the number of solutions for the Sudoku grid.

genPuzzle(): Generates a Sudoku puzzle by removing numbers while ensuring the uniqueness of the solution.

printSVG(string path=""): Prints the Sudoku grid as an SVG file.

branchDifficultyScore(): Calculates the branch difficulty score, which measures the complexity of the Sudoku grid based on the number of branching choices during solving.

calculateDifficulty(): Calculates the difficulty level of the Sudoku puzzle based on the branch difficulty score and the number of empty cells.

Workflow Overview
Initialization:

Upon creation (Sudoku() constructor), the grid is initialized and shuffled.
Seed Generation:

createSeed() method initializes the Sudoku grid by filling diagonal boxes and then solving the grid to ensure it has a unique solution. The solution is stored in solnGrid.
Puzzle Generation:

genPuzzle() method generates a puzzle by removing numbers from the filled grid while ensuring the puzzle remains solvable and has a unique solution.
Difficulty Calculation:

calculateDifficulty() method calculates the difficulty level of the generated puzzle based on how difficult it is to solve.
Output:

printGrid() and printSVG() methods provide different ways to output the current state of the Sudoku grid for display or further processing.
Conclusion
In summary, this code encapsulates the logic for creating, solving, and managing Sudoku puzzles programmatically. It utilizes backtracking for solving, shuffling for puzzle generation, and methods for verifying grid validity and calculating puzzle difficulty. The Sudoku class provides a comprehensive framework for Sudoku puzzle manipulation and interaction, suitable for game development or educational purposes involving Sudoku puzzles.
