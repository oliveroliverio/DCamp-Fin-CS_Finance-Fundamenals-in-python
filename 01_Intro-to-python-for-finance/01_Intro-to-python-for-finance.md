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

```python
# Subset the first three elements
prices_subset_1 = prices_array[0:3]
print(prices_subset_1)
```
```python
# Subset last three elements
prices_subset_2 = prices_array[-3:]
print(prices_subset_2)
```
```python
# Subset every third element
prices_subset_3 = prices_array[0:7:3]
print(prices_subset_3)
```

### [2D arrays and functions](https://campus.datacamp.com/courses/introduction-to-python-for-finance/arrays-in-python?ex=5)

![](img/2021-11-25-18-57-17.png)
![](img/2021-11-25-18-57-35.png)
![](img/2021-11-25-18-57-48.png)
![](img/2021-11-25-18-57-58.png)
![](img/2021-11-25-18-58-12.png)
![](img/2021-11-25-18-58-25.png)
![](img/2021-11-25-18-58-37.png)

### Creating a 2D array

```python
# Create a 2D array of prices and earnings
stock_array = np.array([prices,earnings])
print(stock_array)

# Print the shape of stock_array
print(stock_array.shape)

# Print the size of stock_array
print(stock_array.size)
```
```python
# Transpose stock_array
stock_array_transposed = np.transpose(stock_array)
print(stock_array_transposed)

# Print the shape of stock_array
print(stock_array_transposed.shape)

# Print the size of stock_array
print(stock_array_transposed.size)
```

### [Subsetting 2D arrays](https://campus.datacamp.com/courses/introduction-to-python-for-finance/arrays-in-python?ex=7)

```python
# Subset prices from stock_array_transposed
prices = stock_array_transposed[:, 0]
print(prices)
```

```python
# Subset earnings from stock_array_transposed
earnings = stock_array_transposed[:,1]
print(earnings)
```

```python
# Subset the price and earning for first company
company_1 = stock_array_transposed[0,:]
print(company_1)
```

### [Calculating array stats](https://campus.datacamp.com/courses/introduction-to-python-for-finance/arrays-in-python?ex=8)

```python
# Calculate the mean
prices_mean = np.mean(prices)
print(prices_mean)
```

```python
# Calculate the standard deviation
prices_std = np.std(prices)
print(prices_std)
```

### Generating a sequence of numbers

```python
# Create and print company_ids
company_ids = np.arange(1, 8, 1)
print(company_ids)

# Create and print company_ids_odd
company_ids_odd = np.arange(1, 8, 2)
print(company_ids_odd)
```

### Using arrays for analysis
![](img/2021-11-25-18-54-05.png)
![](img/2021-11-25-18-54-17.png)
![](img/2021-11-25-18-54-38.png)
![](img/2021-11-25-18-55-10.png)
![](img/2021-11-25-18-55-30.png)


### Who's above average?
```python
# Find the mean
price_mean = np.mean(prices)

# Create boolean array
boolean_array = (prices > price_mean)
print(boolean_array)

# Select prices that are greater than average
above_avg = prices[boolean_array]
print(above_avg)
```

### Who's in health care?

```python
# Create boolean array
boolean_array = (sectors == 'Health Care')
print(boolean_array)

# Print only health care companies
health_care = names[boolean_array]
print(health_care)
```

## 4 Visualization in Python

![](img/2021-11-25-19-02-57.png)
![](img/2021-11-25-19-03-26.png)
![](img/2021-11-25-19-03-40.png)
![](img/2021-11-25-19-03-49.png)
![](img/2021-11-25-19-04-02.png)
![](img/2021-11-25-19-04-16.png)
![](img/2021-11-25-19-04-26.png)
![](img/2021-11-25-19-04-48.png)
![](img/2021-11-25-19-04-59.png)
![](img/2021-11-25-19-05-10.png)
![](img/2021-11-25-19-05-33.png)
![](img/2021-11-25-19-05-43.png)
![](img/2021-11-25-19-05-55.png)
![](img/2021-11-25-19-06-03.png)


### In this chapter, you will be introduced to the Matplotlib package for creating line plots, scatter plots, and histograms.

### Visualization in Python

### Importing matplotlib and pyplot

```python
# Import matplotlib.pyplot with the alias plt
import matplotlib.pyplot as plt

# Plot the price of stock over time
plt.plot(days, prices, color="red", linestyle="--")

# Display the plot
plt.show()
```

### Adding axis labels and titles
```python
import matplotlib.pyplot as plt

# Plot price as a function of time
plt.plot(days, prices, color="red", linestyle="--")

# Add x and y labels
plt.xlabel('Days')
plt.ylabel('Prices, $')

# Add plot title
plt.title('Company Stock Prices Over Time')

# Show plot
plt.show()
```

### Multiple lines on the same plot
```python
# Plot two lines of varying colors
plt.plot(days, prices1, color='red')
plt.plot(days, prices2, color='green')

# Add labels
plt.xlabel('Days')
plt.ylabel('Prices, $')
plt.title('Stock Prices Over Time')
plt.show()
```

### Scatterplots
```python
# Import pyplot as plt
import matplotlib.pyplot as plt

# Plot price as a function of time
plt.scatter(days, prices, color='green', s=0.1)

# Show plot
plt.show()
```

### Histograms
![](img/2021-11-25-19-12-30.png)
![](img/2021-11-25-19-12-46.png)
![](img/2021-11-25-19-12-55.png)
![](img/2021-11-25-19-13-04.png)
![](img/2021-11-25-19-13-14.png)
![](img/2021-11-25-19-13-22.png)
![](img/2021-11-25-19-13-33.png)
![](img/2021-11-25-19-13-42.png)
![](img/2021-11-25-19-13-51.png)
![](img/2021-11-25-19-14-01.png)
![](img/2021-11-25-19-14-11.png)
![](img/2021-11-25-19-14-20.png)


### What are applications of histograms in finance?
![](img/2021-11-25-19-14-45.png)

### Is data normally distributed?
```python
# Plot histogram
plt.hist(prices, bins=100)

# Display plot
plt.show()
```

### Comparing two histograms
```python
# Plot histogram of stocks_A
plt.hist(stock_A, bins=100, alpha=0.4)

# Plot histogram of stocks_B
plt.hist(stock_B, bins=100, alpha=0.4)

# Display plot
plt.show()
```

### Adding a legend
```python
# Plot stock_A and stock_B histograms
plt.hist(stock_A, bins=100, alpha=0.4, label='Stock A')
plt.hist(stock_B, bins=100, alpha=0.4, label='Stock B')

# Add the legend
plt.legend()

# Display the plot
plt.show()
```


## 5 S&P 100 Case Study


### In this chapter, you will get a chance to apply all the techniques you learned in the course on the S&P 100 data.

### Introducing the dataset
![](img/2021-11-25-19-20-14.png)
![](img/2021-11-25-19-21-56.png)
![](img/2021-11-25-19-22-09.png)
![](img/2021-11-25-19-22-19.png)
![](img/2021-11-25-19-22-42.png)
![](img/2021-11-25-19-22-52.png)
![](img/2021-11-25-19-23-02.png)
![](img/2021-11-25-19-23-16.png)
![](img/2021-11-25-19-23-28.png)
![](img/2021-11-25-19-24-01.png)


### Lists
```python
# First four items of names
print(names[:4])

# Print information on last company
print(names[-1:])
print(prices[-1:])
print(earnings[-1:])
print(sectors[-1:])
```

### Arrays and NumPy
```python
# Import numpy as np
import numpy as np

# Convert lists to arrays
prices_array = np.array(prices)
earnings_array = np.array(earnings)

# Calculate P/E ratio
pe = prices_array/earnings_array
print(pe)
```

### A closer look at the sectors
![](img/2021-11-25-19-28-18.png)
![](img/2021-11-25-19-28-30.png)
![](img/2021-11-25-19-28-54.png)
![](img/2021-11-25-19-29-02.png)
![](img/2021-11-25-19-29-12.png)



### Filtering arrays

```python
# Create boolean array
boolean_array = (sectors == 'Information Technology')

# Subset sector-specific data
it_names = names[boolean_array]
it_pe = pe[boolean_array]

# Display sector names
print(it_names)
print(it_pe)
```

```python
# Create boolean array
boolean_array = (sectors == 'Consumer Staples')

# Subset sector-specific data
cs_names = names[boolean_array]
cs_pe = pe[boolean_array]

# Display sector names
print(cs_names)
print(cs_pe)
```

### Summarizing sector data
```python
# Calculate mean and standard deviation
it_pe_mean = np.mean(it_pe)
it_pe_std = np.std(it_pe)

print(it_pe_mean)
print(it_pe_std)
```
```python
# Calculate mean and standard deviation
cs_pe_mean = np.mean(cs_pe)
cs_pe_std = np.std(cs_pe)

print(cs_pe_mean)
print(cs_pe_std)
```

### Plot P/E ratios

```python
import matplotlib.pyplot as plt

# Make a scatterplot
plt.scatter(it_id, it_pe, color = 'red', label = 'IT')
plt.scatter(cs_id, cs_pe, color = 'green', label = 'CS')

# Add legend
plt.legend()

# Add labels
plt.xlabel('Company ID')
plt.ylabel('P/E Ratio')
plt.show()
```

### Visualizing trends
![](img/2021-11-25-19-36-29.png)
![](img/2021-11-25-19-36-40.png)

### Histogram of P/E ratios

### Identify the outlier

### Name the outlier

