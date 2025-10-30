# NumPy Program: Replace the Second Column in a 2D Array

## 🎯 Aim
To write a **NumPy** program that deletes the second column from a given 2D array and inserts a new column at the same position.

## 🧠 Algorithm
1. **Import NumPy**: Start by importing the NumPy library.
2. **Get Input**: Get a 2D NumPy array and a new column (as another array) from the user.
3. **Delete Column**: Use `np.delete()` to remove the second column (index 1) from the original array.
4. **Insert Column**: Use `np.insert()` to insert the new column at the second column's original position.
5. **Display Result**: Print the updated array with the replaced column.

## 🧾 Program

```
import numpy as np
arr = np.array([[1, 2, 3],
                [4, 5, 6],
                [7, 8, 9]])

print("Original Array:")
print(arr)
new_col = np.array([10, 11, 12])
arr_deleted = np.delete(arr, 1, axis=1)
arr_updated = np.insert(arr_deleted, 1, new_col, axis=1)
print("\nUpdated Array:")
print(arr_updated)
```

## Output

<img width="392" height="385" alt="image" src="https://github.com/user-attachments/assets/fd01bbfe-2dac-4aed-8b6a-ec0d3becd99e" />


## Result

The code is executed successfully.
