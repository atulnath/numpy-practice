# 📊 NumPy Basics with Examples

This repository contains a step-by-step demonstration of fundamental NumPy concepts in Python, including array creation, indexing, reshaping, operations, and more. This serves as a beginner-friendly reference and hands-on guide.

## 🧮 Environment Setup

```python
import numpy as np
print(np.__version__)
# Output: 2.0.2
📌 Array Creation
python
a = np.array([1, 2, 3])          # Basic 1D array
b = np.zeros((2, 3))            # 2x3 array of zeros
c = np.ones((3, 3))             # 3x3 array of ones
Output:
a: [1 2 3]
b:
[[0. 0. 0.]
 [0. 0. 0.]]
c:
[[1. 1. 1.]
 [1. 1. 1.]
 [1. 1. 1.]]
👁 Eye, Arange, Linspace
np.eye(4)                       # Identity matrix
np.arange(10)                   # Array from 0 to 9
np.linspace(0, 1, 6)            # 6 evenly spaced values between 0 and 1
Output:
eye:
[[1. 0. 0. 0.]
 [0. 1. 0. 0.]
 [0. 0. 1. 0.]
 [0. 0. 0. 1.]]
arange: [0 1 2 3 4 5 6 7 8 9]
linspace: [0.  0.2 0.4 0.6 0.8 1. ]
🔍 Indexing & Slicing
arr = np.array([[10, 20, 30], [40, 50, 60]])

arr[0, 1]       # Single element
arr[:, 1]       # Second column
arr[1, :2]      # First two elements from second row
Output:
20
[20 50]
[40 50]
➕ Array Math & Operations
a = np.array([1, 2, 3])
b = np.array([4, 5, 6])

a + b
a * b
np.dot(a, b)
Output:
[5 7 9]
[ 4 10 18]
32
✅ Boolean Indexing & Filtering
python
Copy
Edit
arr = np.array([1, 5, 7, 9, 2])
arr[arr > 5]
Output:
[7 9]
📊 Aggregation & Statistics
a = np.array([[1, 2, 3], [4, 5, 6]])
np.sum(arr)
np.mean(arr, axis=0)
Output:
Sum: 24
Mean: 4.8
🔄 Reshape, Stack & Split
arr = np.arange(12)
reshaped = arr.reshape((3, 4))

v_stack = np.vstack([arr, arr])
h_split = np.hsplit(reshaped, 2)
Output:

reshaped:
[[ 0  1  2  3]
 [ 4  5  6  7]
 [ 8  9 10 11]]

v_stack:
[[ 0  1  2 ... 11]
 [ 0  1  2 ... 11]]

h_split:
[array([[0, 1], [4, 5], [8, 9]]), 
 array([[ 2,  3], [ 6,  7], [10, 11]])]
