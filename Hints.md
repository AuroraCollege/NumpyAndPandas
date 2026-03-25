## Numpy Hints

### Task 1: Create a Linear Dataset

```python
feature = np.arange(6, 21)
print(feature)
label = (feature * 3) + 4
print(label)
```

### Task 2: Add Some Noise to the Dataset
```python
noise = (np.random.random([15]) * 4) - 2
print(noise)
label = label + noise
print(label)
```

## Pandas Hints

### Task 1: Create a DataFrame
```python
#@title Double-click for a solution to Task 1.

# Create a Python list that holds the names of the four columns.
my_column_names = ['Eleanor', 'Chidi', 'Tahani', 'Jason']

# Create a 3x4 numpy array, each cell populated with a random integer.
my_data = np.random.randint(low=0, high=101, size=(3, 4))

# Create a DataFrame.
df = pd.DataFrame(data=my_data, columns=my_column_names)

# Print the entire DataFrame
print(df)

# Print the value in row #1 of the Eleanor column.
print("\nSecond row of the Eleanor column: %d\n" % df['Eleanor'][1])

# Create a column named Janet whose contents are the sum
# of two other columns.
df['Janet'] = df['Tahani'] + df['Jason']

# Print the enhanced DataFrame
print(df)
```
