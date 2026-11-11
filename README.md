# NumPy Fundamentals

A beginner-friendly introduction to common operations with NumPy, Python's library for working with numerical arrays. The accompanying [`numpy_foundmentals.ipynb`](./numpy_foundmentals.ipynb) notebook contains examples.

## Install NumPy

```bash
python -m pip install numpy
```

## Create arrays

```python
import numpy as np

numbers = np.array([1, 2, 3])
matrix = np.array([[1, 2, 3], [4, 5, 6]])
zeros = np.zeros((2, 3))
sequence = np.arange(0, 10, 2)
```

NumPy arrays have a `shape` and a data type:

```python
print(matrix.shape)  # (2, 3)
print(matrix.dtype) # e.g. int32 or int64
```

## Arithmetic and broadcasting

Operations on arrays are applied element by element. NumPy can also broadcast compatible shapes, such as adding one value to every element:

```python
values = np.array([10, 20, 30])
print(values + 2)  # [12 22 32]
print(values * 3)  # [30 60 90]

left = np.array([1, 2, 3])
right = np.array([4, 5, 6])
print(left + right)  # [5 7 9]
```

## Indexing and slicing

```python
print(values[0])       # First element: 10
print(values[1:])      # Elements from index 1 onward
print(matrix[0, 1])    # Row 0, column 1: 2
print(matrix[:, 0])    # First column
```

## Aggregations

```python
scores = np.array([[80, 75, 90], [95, 92, 88]])

print(np.sum(scores))            # Sum of all scores
print(np.mean(scores))           # Mean of all scores
print(np.max(scores))            # Largest score
print(np.sum(scores, axis=1))    # Sum of each row
print(np.mean(scores, axis=0))   # Mean of each column
```

For a 2D array, `axis=0` reduces down the rows (one result per column), and `axis=1` reduces across the columns (one result per row).

## Reshape and filter

```python
sequence = np.arange(1, 7)
grid = sequence.reshape(2, 3)
print(grid)

print(sequence[sequence > 3])  # [4 5 6]
```

## Resources

- [NumPy documentation](https://numpy.org/doc/)
- [NumPy quickstart](https://numpy.org/doc/stable/user/quickstart.html)
