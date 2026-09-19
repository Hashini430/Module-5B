# Module 5B - Combined Programming Exercises

This file combines the NumPy and Pandas exercise notes currently present in Module 5B into a single document that can be exported to PDF.

---

# 1. NumPy Program: Column-wise Sorting of a 2D Array

## 🎯 Aim
To write a NumPy program that sorts the elements in each column of a given 2D array in ascending order.

## 🧠 Algorithm
1. Import NumPy.
2. Get input: Accept a 2D NumPy array from the user.
3. Sort column-wise: Use `np.sort()` with `axis=0` to sort each column in ascending order.
4. Store the result in a new array.
5. Display the original array and the sorted array.

## 🧾 Program
```python
import numpy as np

a=np.array(eval(input()))

print("Given array")
print(end=" ")
print(a)
print()
print(np.sort(a,axis=0))
```

## Output
<img width="578" height="239" alt="image" src="https://github.com/user-attachments/assets/6abc8045-1b32-49a8-868b-6fc75f217538" />

## Result
Thus the Python program for sorting each column in NumPy has been implemented and executed successfully.

---

# 2. NumPy Program: Find Indices Where Elements in Array x are Greater Than or Equal to Corresponding Elements in Array y

## 🎯 Aim
To write a Python program using NumPy that finds the indices where elements in array `x` are greater than or equal to their corresponding elements in array `y`.

## 🧠 Algorithm
1. Import NumPy.
2. Define two NumPy arrays, `x` and `y`, with the same shape.
3. Use boolean indexing:
   - `x > y` gives a boolean array where elements of `x` are greater than `y`.
   - `x == y` gives a boolean array where elements of `x` are equal to `y`.
4. Find indices with `np.where()` for the condition `x >= y`.
5. Print the indices.

## 🧾 Program
```python
import numpy as np

x=eval(input())
y=eval(input())

l1=np.array(x)
l2=np.array(y)

print(np.where(l1>l2))
print(np.where(l1==l2))
```

## Output
<img width="583" height="162" alt="image" src="https://github.com/user-attachments/assets/871713b7-5e9d-4bfa-917f-6332c070ed18" />

## Result
Thus the Python program for element-wise comparison between two NumPy arrays has been implemented and executed successfully.

---

# 3. NumPy Program: Replace the Second Column in a 2D Array

## 🎯 Aim
To write a NumPy program that deletes the second column from a given 2D array and inserts a new column at the same position.

## 🧠 Algorithm
1. Import NumPy.
2. Get input: Get a 2D NumPy array and a new column array from the user.
3. Delete the second column using `np.delete()`.
4. Insert the new column at the second position using `np.insert()`.
5. Display the updated array.

## 🧾 Program
```python
import numpy as np

a=np.array(eval(input()))
b=np.array(eval(input()))

print("Printing Original array")
print(a)

print("Array after deleting column 2 on axis 1")
c=np.delete(a,1,axis=1)
print(c)

print("Array after inserting column 2 on axis 1")
print(np.insert(c,1,b,axis=1))
```

## Output
<img width="690" height="203" alt="image" src="https://github.com/user-attachments/assets/5df9fafc-7f8d-442b-9b4b-25003d6b1c7d" />

## Result
Thus the Python program for replacing a column in NumPy has been implemented and executed successfully.

---

# 4. Pandas Program: Create and Display a DataFrame with Custom Index Labels

## 🎯 Aim
To create and display a DataFrame using the Pandas library in Python from a given dictionary, and apply specific index labels to the rows.

## 🧠 Algorithm
1. Import the required libraries: `pandas` and `numpy`.
2. Create the dictionary `exam_data` with keys: `name`, `score`, `attempts`, and `qualify`.
3. Create a list of custom index labels called `labels`.
4. Create the DataFrame using `pd.DataFrame()` and pass both the dictionary and `index=labels`.
5. Display the DataFrame.

## 💻 Program
```python
import pandas as pd
import numpy as np

exam_data = {'name': ['Anastasia', 'Dima', 'Katherine', 'James', 'Emily', 'Michael', 'Matthew', 'Laura', 'Kevin', 'Jonas'],
             'score': [12.5, 9, 16.5, np.nan, 9, 20, 14.5, np.nan, 8, 19],
             'attempts': [1, 3, 2, 3, 2, 3, 1, 1, 2, 1],
             'qualify': ['yes', 'no', 'yes', 'no', 'no', 'yes', 'yes', 'no', 'no', 'yes']}

labels = ['a', 'b', 'c', 'd', 'e', 'f', 'g', 'h', 'i', 'j']

df = pd.DataFrame(exam_data, index=labels)

print(df)
```

## Output
<img width="672" height="322" alt="image" src="https://github.com/user-attachments/assets/a56a6300-57fd-47ca-b3b4-438945600a9f" />

## Result
Thus, the Python program has been created and executed successfully to create a DataFrame using the given dictionary and index labels and displayed.

---

# 5. Pandas Program: Join Two DataFrames Along Rows

## 🎯 AIM
To write a Python program using Pandas to join two DataFrames along rows (row-wise concatenation) and assign all data to a new DataFrame.

## 🧠 ALGORITHM
1. Import the `pandas` library.
2. Create the first DataFrame: `student_data1`.
3. Create the second DataFrame: `student_data2`.
4. Concatenate DataFrames using `pd.concat()` with `axis=0`.
5. Display the resulting DataFrame.

## 💻 Program
```python
import pandas as pd

student_data1 = pd.DataFrame({
    'student_id': ['S1', 'S2', 'S3', 'S4', 'S5'],
    'name': ['Danniella Fenton', 'Ryder Storey', 'Bryce Jensen', 'Ed Bernal', 'Kwame Morin'],
    'marks': [200, 210, 190, 222, 199]
})

student_data2 = pd.DataFrame({
    'student_id': ['S4', 'S5', 'S6', 'S7', 'S8'],
    'name': ['Scarlette Fisher', 'Carla Williamson', 'Dante Morse', 'Kaiser William', 'Madeeha Preston'],
    'marks': [201, 200, 198, 219, 201]
})

print("Original DataFrames:")
print(student_data1)
print("-------------------------------------")
print(student_data2)
print("\nJoin the said two dataframes along rows:")

result_data = pd.concat([student_data1, student_data2])
print(result_data)
```

## Output
<img width="694" height="855" alt="image" src="https://github.com/user-attachments/assets/d62ef81d-bdab-44ed-bc87-ca4a690d328e" />

## Result
Thus, the Python program has been successfully created and executed to join the two DataFrames row-wise using `pd.concat()` and all records from both DataFrames were included in the final result.

---

# Conclusion
These exercises cover NumPy arrays and Pandas DataFrames, including sorting, comparison, column replacement, DataFrame creation, and row-wise concatenation. The combined file is ready to be reviewed and exported to PDF.
