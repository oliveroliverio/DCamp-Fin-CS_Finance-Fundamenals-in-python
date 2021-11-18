# [Introduction to Python for Finance](https://app.datacamp.com/learn/courses/introduction-to-python-for-finance)


## 1 Welcome to Python

This chapter is an introduction to basics in Python, including how to name variables and various data types in Python.

### Welcome to Python for Finance!

### Why might you use Python in finance?

### Run code vs. submit answer

### Comments and variables

### Printing output

### Finding the average revenue

### Data types

### Creating variables

### Determining types

### Booleans in Python

### Combining data types


## 2 Lists


### This chapter introduces lists in Python and how they can be used to work with data.

### Lists

### Creating lists in Python

### Indexing list items

### Slicing multiple list elements

### Nested lists

### Stock up a nested list

### Subset a nested list

### List methods and functions

### Exploring list methods and functions

- Sort this list
```python
# Print the sorted list prices
prices = [159.54, 37.13, 71.17]
prices.sort()
print(prices)
```

- find max price of list
```python
# Find the maximum price in the list price
prices = [159.54, 37.13, 71.17]
price_max = max(prices)
print(price_max)
```

### Using list methods to add data

```python
# Append a name to the list names
names.append('Amazon.com')
print(names)

# Extend list names
more_elements = ['DowDuPont', 'Alphabet Inc']
names.extend(more_elements)
print(names)
```

### Finding stock with maximum price
- using index of list to find max price

```python
# Do not modify this
max_price = max(prices)

# Identify index of max price
max_index = prices.index(max_price)

# Identify the name of the company with max price
max_stock_name = names[max_index]

# Fill in the blanks
print('The largest stock price is associated with ' + max_stock_name + ' and is $' + str(max_price) + '.')
```

## 3 Arrays in Python
- create arrays using the np.array() function

### [Create an array](https://campus.datacamp.com/courses/introduction-to-python-for-finance/arrays-in-python?ex=2)
```python
# Import numpy as np
import numpy as np

# Lists
prices = [170.12, 93.29, 55.28, 145.30, 171.81, 59.50, 100.50]
earnings = [9.2, 5.31, 2.41, 5.91, 15.42, 2.51, 6.79]

# NumPy arrays
prices_array = np.array(prices)
earnings_array = np.array(earnings)

# Print the arrays
print(prices_array)
print(earnings_array)
```

### [Elementwise operations on arrays](https://campus.datacamp.com/courses/introduction-to-python-for-finance/arrays-in-python?ex=3)
```python
# Import numpy as np
import numpy as np

# Create PE ratio array
pe_array = prices_array/earnings_array

# Print pe_array
print(pe_array)
```

### [Subsetting elements from an array](https://campus.datacamp.com/courses/introduction-to-python-for-finance/arrays-in-python?ex=4)

### 2D arrays and functions

### Creating a 2D array

### Subsetting 2D arrays

### Calculating array stats

### Generating a sequence of numbers

### Using arrays for analysis

### Who's above average?

### Who's in health care?


## 4 Visualization in Python


### In this chapter, you will be introduced to the Matplotlib package for creating line plots, scatter plots, and histograms.

### Visualization in Python

### Importing matplotlib and pyplot

### Adding axis labels and titles

### Multiple lines on the same plot

### Scatterplots

### Histograms

### What are applications of histograms in finance?

### Is data normally distributed?

### Comparing two histograms

### Adding a legend


## 5 S&P 100 Case Study


### In this chapter, you will get a chance to apply all the techniques you learned in the course on the S&P 100 data.

### Introducing the dataset

### Lists

### Arrays and NumPy

### A closer look at the sectors

### Filtering arrays

### Summarizing sector data

### Plot P/E ratios

### Visualizing trends

### Histogram of P/E ratios

### Identify the outlier

### Name the outlier

