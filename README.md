I've created a beginner-friendly NumPy Basics README covering installation, arrays, indexing, slicing, mathematical operations, reshaping, broadcasting, aggregation, and practical examples.

Ready to saveWriting

# NumPy Basics – Beginner's Guide

A beginner-friendly introduction to NumPy in Python.

## 1\. What is NumPy?

NumPy (Numerical Python) is a Python library used for numerical computing.

It provides:

- Fast mathematical operations.
- Multidimensional arrays.
- Matrix operations.
- Statistical calculations.
- Data manipulation tools.

## 2\. Installation

Install NumPy using pip:

bash

```bash
pip install numpy
```

Import NumPy:

python

```python
import numpy as np
```

## 3\. Creating NumPy Arrays

### Create a 1D array

python

```python
import numpy as np

arr = np.array([10, 20, 30, 40, 50])
print(arr)
```

### Create a 2D array

python

```python
arr = np.array([
    [1, 2, 3],
    [4, 5, 6]
])

print(arr)
```

### Create arrays using built-in functions

python

```python
np.zeros((2, 3))       # Array of zeros
np.ones((3, 3))        # Array of ones
np.full((2, 2), 7)     # Array filled with 7
np.eye(3)              # Identity matrix
np.arange(1, 10)       # Numbers from 1 to 9
np.linspace(0, 10, 5)  # Five equally spaced values
```

## 4\. Array Attributes

python

```python
arr = np.array([[1, 2, 3], [4, 5, 6]])

print(arr.ndim)    # Number of dimensions
print(arr.shape)   # Shape of array
print(arr.size)    # Total number of elements
print(arr.dtype)   # Data type
```

## 5\. Indexing and Slicing

### Indexing

python

```python
arr = np.array([10, 20, 30, 40, 50])

print(arr[0])   # 10
print(arr[2])   # 30
print(arr[-1])  # 50
```

### Slicing

python

```python
print(arr[1:4])  # [20 30 40]
print(arr[:3])   # First three elements
print(arr[2:])   # From index 2
print(arr[::2])  # Every second element
```

### 2D Array Indexing

python

```python
arr = np.array([[1, 2, 3],
                [4, 5, 6]])

print(arr[0, 1])  # 2
print(arr[1, 2])  # 6
print(arr[:, 0])  # First column
print(arr[0, :])  # First row
```

## 6\. Mathematical Operations

NumPy supports vectorized mathematical operations.

python

```python
a = np.array([10, 20, 30])
b = np.array([1, 2, 3])

print(a + b)
print(a - b)
print(a * b)
print(a / b)
print(a ** 2)
```

### Scalar Operations

python

```python
arr = np.array([1, 2, 3, 4])

print(arr + 10)
print(arr * 2)
print(arr / 2)
```

## 7\. Aggregate Functions

python

```python
arr = np.array([10, 20, 30, 40, 50])

print(np.sum(arr))
print(np.mean(arr))
print(np.median(arr))
print(np.min(arr))
print(np.max(arr))
print(np.std(arr))
print(np.var(arr))
```

## 8\. Reshaping Arrays

Change the shape of an array without changing its data.

python

```python
arr = np.arange(1, 13)

new_arr = arr.reshape(3, 4)

print(new_arr)
```

Output:

text

```text
[[ 1  2  3  4]
 [ 5  6  7  8]
 [ 9 10 11 12]]
```

Flatten an array:

python

```python
arr.flatten()
```

## 9\. Joining and Splitting Arrays

### Concatenate

python

```python
a = np.array([1, 2, 3])
b = np.array([4, 5, 6])

result = np.concatenate((a, b))
print(result)
```

### Vertical and Horizontal Stacking

python

```python
np.vstack((a, b))
np.hstack((a, b))
```

### Splitting

python

```python
arr = np.array([1, 2, 3, 4, 5, 6])

result = np.split(arr, 3)
print(result)
```

## 10\. Broadcasting

Broadcasting allows NumPy to perform operations on arrays with compatible shapes.

python

```python
arr = np.array([1, 2, 3])

print(arr + 10)
```

Output:

text

```text
[11 12 13]
```

Example with a 2D array:

python

```python
arr = np.array([[1, 2, 3],
                [4, 5, 6]])

print(arr + np.array([10, 20, 30]))
```

## 11\. Boolean Filtering

Filter array elements based on conditions.

python

```python
arr = np.array([10, 20, 30, 40, 50])

print(arr[arr > 25])
```

Output:

text

```text
[30 40 50]
```

Other examples:

python

```python
print(arr[arr < 30])
print(arr[arr == 20])
print(arr[arr % 2 == 0])
```

## 12\. Random Numbers

python

```python
np.random.rand(3)          # Random floats
np.random.randint(1, 100, 5)  # Random integers
np.random.randn(3)         # Standard normal values
np.random.seed(42)         # Reproducible results
```

## 13\. Linear Algebra

NumPy provides useful matrix operations.

python

```python
a = np.array([[1, 2],
              [3, 4]])

b = np.array([[5, 6],
              [7, 8]])

print(np.dot(a, b))      # Matrix multiplication
print(np.linalg.det(a)) # Determinant
print(np.linalg.inv(a)) # Inverse
print(a.T)               # Transpose
```

For matrix multiplication, you can also use:

python

```python
print(a @ b)
```

## 14\. Practical Example

Calculate the average marks of students.

python

```python
import numpy as np

marks = np.array([
    [80, 85, 90],
    [70, 75, 80],
    [90, 95, 85]
])

# Average marks of each student
student_avg = np.mean(marks, axis=1)

# Average marks of each subject
subject_avg = np.mean(marks, axis=0)

# Highest and lowest marks
highest = np.max(marks)
lowest = np.min(marks)

print("Student averages:", student_avg)
print("Subject averages:", subject_avg)
print("Highest marks:", highest)
print("Lowest marks:", lowest)
```

## 15\. Important NumPy Functions Cheat Sheet

| Function | Purpose |
| --- | --- |
| `np.array()` | Create an array |
| `np.zeros()` | Create zero array |
| `np.ones()` | Create one array |
| `np.arange()` | Generate number sequence |
| `np.linspace()` | Generate evenly spaced numbers |
| `np.reshape()` | Change array shape |
| `np.sum()` | Calculate sum |
| `np.mean()` | Calculate average |
| `np.median()` | Calculate median |
| `np.std()` | Standard deviation |
| `np.max()` | Maximum value |
| `np.min()` | Minimum value |
| `np.sort()` | Sort elements |
| `np.unique()` | Find unique values |
| `np.concatenate()` | Join arrays |
| `np.where()` | Conditional selection |
| `np.transpose()` | Transpose array |
| `np.dot()` | Dot product |

## 16\. Practice Exercises

Try solving these exercises yourself.

1. Create a NumPy array containing numbers from 1 to 20.
2. Find the sum and average of an array.
3. Create a 3×3 matrix containing numbers from 1 to 9.
4. Extract the first row and second column of a matrix.
5. Find all even numbers in an array.
6. Sort an array in ascending order.
7. Reshape an array of 12 elements into a 3×4 matrix.
8. Find the maximum and minimum values.
9. Generate 10 random integers between 1 and 100.
10. Calculate the average marks of five students.

## 17\. Recommended Learning Path

1. Understand Python lists and basic Python syntax.
2. Learn NumPy array creation.
3. Practice indexing and slicing.
4. Learn mathematical operations.
5. Understand broadcasting.
6. Practice aggregation and statistics.
7. Learn reshaping and matrix operations.
8. Build small numerical projects.

## Conclusion

NumPy is one of the most important Python libraries for data science, machine learning, scientific computing, and data analysis.

Mastering these basics will prepare you for libraries such as Pandas, Matplotlib, Scikit-learn, and TensorFlow.

**Happy Learning\!**

How to download: Open the document above and use the available copy/export option to save it as `README.md` in your project folder.
