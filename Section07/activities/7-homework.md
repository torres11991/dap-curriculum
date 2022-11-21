# 7. Python Homework

## NumPy, Pandas, and MatPlotlib

Create a file and name it 7-Homework (this should be a Jupyter Notebook file so you can write MarkDown and Python code)

<br>

### **Please Answer These Questions:-**

1. What does one need to do to use a module?
1. Name a Module (not the DateTime Nodule) we looked at and write a line or 2 of code as an example using this module.
1. What is a benefit of using Exception handling?
1. NumPy arrays are like what Python data type?
1. What is one of the main benefits of using NumPy arrays.
1. What is one of the main requirements about the 'dtype' of NumPy arrays?
1. Of the 10 uses of NumPy, name 2.
1. Name one of the other libraries we'll use with NumPy?
1. What is the shape of NumPy arrays?
1. What is a Tensor?
1. Name a reason why it's better using  NumPy for Data Analysis than using a Python List?
1. When creating an "empty" array, where do the elements come from?
1. What does Pandas stand for?
1. What are the 2 collections used in Pandas?
1. Name 4 things Pandas can do for us.
1. To permanently sort a DataFrame, which keyword should one use with the `df.sort()` method?
1. What is a CSV
1. When cleaning data what values do we not like in our data?

<br>

### **Please Complete this Coding Exercise:-**

1. Concatenate these 3 arrays into a new array named 'newArray'...

```python
        ([[25, 16]])
        ([[11, 2], [13, 4]])
        ([[7, 81], [5, 6], [11, 12]])
```

2. Sort 'newArray' in order into 'sortedArray'

3. Reshape the 'sortedArray' array, into a new array called 'reshapedArray', so it has 2 dimensions with a size of 2, 3.

4. Unpack the array tuples from the above 'reshapedArray'  into 4 well named variables. Print the 4 variables.

5. Combined and sort the following arrays into one called 'comboArray' ...

```python
    one = ([10, 11, 12, 13, 14, 15, 16, 17])
    two = ([20, 21, 22, 23, 24, 25, 26, 27])
    three = ([ 0, 1, 2, 3, 4, 5, 6, 7])
```

6.  Take 'comboArray' and perform the following slicing activities:
    - print sec1 - the 2nd element
    - print sec2 - all elements from the 3rd element to the last
    - print sec3 - all elements from the 4th to the 14th elements
    - print sec4 - the last 6 elements
    - print sec5 - all element from #0 up to and including #15, using the negative number method, i.e. taking a section from the end.
    - print sec6 - from #20 every even element to the end
    - print sec7 - from the last element moving forward, every 5th element.

<br>

7. Using simple math operations, broadcast the addition `(+)`, division `(/)`, and multiplication `(*)` operations for these 2 arrays --

```python
    ([[[ 0.0,  0.0,  0.10], [10.0, 10.30, 10.01]],
        [[20.0, 20.02, 20.10], [30.0, 31.0, 30.30]],
        [[40.40, 24.0, 40.0], [15.0, 15.5, 25.5]]])

    ([[17.0, 70.0, 10.7]])
```

8. Use the NumPy Arithmetic functions to do the subtraction of the above two arrays in pont #7.

9. Using modulo find all elements that are divisible by 3 from the multi-dimensional array under point #7 above.

10. Using `Series`, create a `DataFrame` that looks like this:

    | Ingredients | Quantity | Unit |
    |----|----|----|
    | Flour | 4 | cups |
    | Milk | 1 | cup |
    | Eggs | 2 | large |
    | Spam | 1 | can |

    Name: Dinner, dtype: object

<br>

11. Take this data and create a DataFrame named studentData

```Python
    {'Name': ['Jai', 'janusha', 'Gaurav', 'Anuj'],
        'Height': [5.1, 6.2, 5.1, 5.2],
        'Qualification': ['Msc', 'MA', 'Msc', 'Msc'],
        'address': ['Delhi', 'Doha', 'Chennai', 'Dakhar'],
        'Age': [21, 23, 24, 21],
        'Pets': ['Dog', 'Bunny', 'Chinchilla', 'Parrot'],
        'sport': ['Darts', 'Basketball', 'PaddleBoarding', 'Cricket']
    }
```

<br>

12. Add a new column to the DataFrame with the following deserts:
        ["ice cream", "Cashew Fudge", "waffels", "Carrot Halwa"]

13. Sort the 'studentData' DataFrame in Ascending order -- Sorting by column 'Name' and then "address"

14. Save this `DataFrame` here below to disc as a `.CSV` file with the name `cows_and_goats.csv`:

```python
    df = pd.DataFrame({'Cows': [12, 20], 'Goats': [22, 19]}, index=['Year 1', 'Year 2'])
```

15. (A) Using Pandas, make your own .CSV file with data on vegetables and save it. (B) Using Pandas, make a change to your CSV file, and save a copy with a different name.

<br>

### **When done with homework:-**

When homework has been completed, do the following...

- Make sure your homework file is well named
- Add the homework to your Homework folder
- Use  git add, git commit, and git push to upload your homework changes to GitHub in the cloud
- Create a ticket in Jira to indicate that your Homework is ready for review
