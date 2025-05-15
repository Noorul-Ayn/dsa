# Sparse Matrix Operations

## Overview

This project implements a memory-efficient data structure for representing **sparse matrices** and performing **addition**, **subtraction**, and **multiplication** operations on them.

The sparse matrix data is read from input files in a custom format, and the program avoids using standard template libraries or built-in advanced utilities like `regex`, as per the assignment rules.

## Directory Structure

```

/dsa/sparse\_matrix/
│
├── code/
│   └── src/
│       └── sparse\_matrix.js (or .cpp, .py etc.)
│
└── sample\_inputs/
├── matrix1.txt
└── matrix2.txt

```

> **Note**: You can restructure the project directory if desired.

---

## Input Format

Each sparse matrix file should be in the following format:

```

rows=8433
cols=3180
(0, 381, -694)
(0, 128, -838)
(0, 639, 857)
...

```

- The first line specifies the number of **rows**.
- The second line specifies the number of **columns**.
- Each subsequent line represents a non-zero matrix entry in the format: `(rowIndex, colIndex, value)`.

### Input Rules:
- Whitespaces in lines should be ignored.
- If invalid syntax is detected (e.g. wrong parenthesis, floats), throw an error:
```

std::invalid\_argument("Input file has wrong format")

````

---

## Features

- Read sparse matrices from files
- Perform matrix **addition**, **subtraction**, and **multiplication**
- Handle and report input format errors
- Efficient custom data structures for space and time optimization
- Interactive CLI for user to choose operations
- No use of standard library data structures or utilities like `regex`

---

## Classes and Methods

### SparseMatrix Class

```cpp
SparseMatrix(char* matrixFilePath)          // Constructor to load from file
SparseMatrix(int numRows, int numCols)      // Constructor to initialize empty matrix
getElement(int row, int col)                // Returns value at specified position
setElement(int row, int col, int value)     // Sets a non-zero value at a position
add(SparseMatrix other)                     // Returns new SparseMatrix as result
subtract(SparseMatrix other)                // Returns new SparseMatrix as result
multiply(SparseMatrix other)                // Returns new SparseMatrix as result
````

> Helper functions and custom data structures are allowed.

---

## How to Use

1. **Compile/Run** the program.
2. When prompted, **select the matrix operation** to perform:

   * Addition
   * Subtraction
   * Multiplication
3. Provide the **file paths** for the two matrices (e.g. `../sample_inputs/matrix1.txt`).
4. The result will be computed and output (to file or terminal based on implementation).

---

## Exception Handling

* Ensure matrices are compatible for the operation (e.g. matching dimensions for addition/subtraction, valid sizes for multiplication).
* If not, raise descriptive errors and stop execution.

---

## Notes

* Reuse of **self-written** or **class-provided** code is allowed, but must be **documented and cited**.
* Do **not** use built-in libraries for parsing or matrix operations.
* Matrix operations must be **manually implemented**.

---

## Sample Output

A result file or console output should follow the same format as input:

```
rows=8433
cols=3180
(0, 128, 22)
(0, 639, 345)
...
```

---

## Author

*Student Name*: \[Hauwa Bello]

```
