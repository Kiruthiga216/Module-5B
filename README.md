# NumPy Program: Column-wise Sorting of a 2D Array

## 🎯 Aim
To write a **NumPy** program that sorts the elements in each column of a given 2D array in ascending order.

## 🧠 Algorithm

1. **Import NumPy**: Start by importing the NumPy library.
2. **Get Input**: Accept a 2D NumPy array from the user.
3. **Sort Column-wise**: Use the `np.sort()` function with `axis=0` to sort each column in ascending order.
4. **Store Result**: Store the sorted result in a new array.
5. **Display Output**: Print the original array and the column-wise sorted array.

## 🧾 Program

```
import numpy as np
arr = np.array([[9, 2, 7],
                [4, 5, 6],
                [1, 8, 3]])

print("Original Array:")
print(arr)
sorted_arr = np.sort(arr, axis=0)
print("\nColumn-wise Sorted Array:")
print(sorted_arr)
```

## Output

<img width="368" height="376" alt="image" src="https://github.com/user-attachments/assets/6531c064-91d5-45a4-ab66-6c8d84d214c7" />


## Result

The code is executed successfully.

# # NumPy Program: Find Indices Where Elements in Array x are Greater Than or Equal to Corresponding Elements in Array y

## 🎯 Aim
To write a Python program using **NumPy** that finds the indices where elements in array `x` are greater than or equal to their corresponding elements in array `y`.

## 🧠 Algorithm
1. **Import NumPy**: Import the NumPy library.
2. **Define Arrays**: Define two NumPy arrays, `x` and `y`, with the same shape (i.e., same number of elements).
3. **Use Boolean Indexing**: 
   - `x > y` gives a boolean array where elements of `x` are greater than `y`.
   - `x == y` gives a boolean array where elements of `x` are equal to `y`.
4. **Find Indices**: Use `np.where()` to get the indices where the conditions `x >= y` are satisfied.
5. **Print Indices**: Print the indices where the condition holds true.

## 🧾 Program

```
import numpy as np
x = np.array([4, 7, 1, 8, 5])
y = np.array([3, 7, 2, 5, 6])
print("Array x:", x)
print("Array y:", y)
indices = np.where(x >= y)
print("Indices where x >= y:", indices[0])
```

## Output

<img width="369" height="184" alt="image" src="https://github.com/user-attachments/assets/7a5e1d96-865d-4948-8543-16ca0d97a696" />


## Result

The code is executed successfully.


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


# Pandas Program: Create and Display a DataFrame with Custom Index Labels

## 🎯 Aim

To create and display a **DataFrame** using the **Pandas** library in Python from a given dictionary, and apply specific index labels to the rows.

---

## 🧠 Algorithm

1. **Import Libraries**: Import the required libraries – `pandas` and `numpy`.
2. **Create Dictionary**: Define a dictionary `exam_data` with keys: `'name'`, `'score'`, `'attempts'`, and `'qualify'`.
3. **Index Labels**: Create a list of custom index labels called `labels`.
4. **Create DataFrame**: Use `pd.DataFrame()` to create the DataFrame by passing the dictionary and index labels.
5. **Display Output**: Display the DataFrame using `print()` or by simply calling the DataFrame variable.

---

## 💻 Program

```
import pandas as pd
import numpy as np
exam_data = {
    'name': ['Anastasia', 'Dima', 'Katherine', 'James', 'Emily', 'Michael', 'Matthew', 'Laura', 'Kevin', 'Jonas'],
    'score': [12.5, 9, 16.5, 12, 9, 20, 14.5, 13, 8, 19],
    'attempts': [1, 3, 2, 3, 2, 3, 1, 1, 2, 1],
    'qualify': ['yes', 'no', 'yes', 'no', 'no', 'yes', 'yes', 'no', 'no', 'yes']
}
labels = ['a', 'b', 'c', 'd', 'e', 'f', 'g', 'h', 'i', 'j']
df = pd.DataFrame(exam_data, index=labels)
print("DataFrame with custom index labels:")
print(df)
```

## Output

<img width="410" height="454" alt="image" src="https://github.com/user-attachments/assets/7d0f22c0-ab10-41c4-96fa-fc5c2fbe139b" />


## Result

The code is executed successfully.

# 🧪 Pandas Program: Join Two DataFrames Along Rows

## 🎯 AIM

To write a Python program using Pandas to **join two DataFrames along rows** (row-wise concatenation) and assign all data to a new DataFrame.

---

## 🧠 ALGORITHM

1. **Import Libraries**: Import the `pandas` library.
2. **Create First DataFrame**: Use a dictionary to create `student_data1`.
3. **Create Second DataFrame**: Use another dictionary to create `student_data2`.
4. **Concatenate DataFrames**: Use `pd.concat()` with `axis=0` to concatenate both DataFrames row-wise.
5. **Display Result**: Print the new combined DataFrame.

---

## 💻 Program

```
import pandas as pd
student_data1 = {
    'ID': [1, 2, 3, 4],
    'Name': ['Alice', 'Bob', 'Charlie', 'David'],
    'Grade': ['A', 'B', 'C', 'B']
}
df1 = pd.DataFrame(student_data1)
student_data2 = {
    'ID': [5, 6, 7, 8],
    'Name': ['Eva', 'Frank', 'Grace', 'Hannah'],
    'Grade': ['A', 'C', 'B', 'A']
}
df2 = pd.DataFrame(student_data2)
combined_df = pd.concat([df1, df2], axis=0)
print("Row-wise Concatenated DataFrame:")
print(combined_df)
```

## Output

<img width="369" height="390" alt="image" src="https://github.com/user-attachments/assets/184c85c0-da8c-4912-a6ba-1a3d5a05b826" />


## Result

The code is executed successfully.
