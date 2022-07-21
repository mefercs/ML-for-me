# TF first steps
## Numpy gold concepts 
import and create a simple array
```py 
import numpy as np
one_dim = np.array([1,2,3,4])
#Two dimensions
two_dim = np.array([[1,2,3],[4,5,6],[7,8,9]])
```
To populate with only zeros and ones
```py 
ones = np.ones(8) #an array with 8 ones
zeros = np.zeros(8) #an array with 8 zeros
```
Create an array within a range of value 
```py
sequence = np.arange(5,15) # 5 - 14 because 15 is non-inclusive
sequence = np.arange(5,15,3) # 5 - 14 with steps of 3
sequence = np.linspace(begin, end, num="number of partitions")
```
Create a range of random numbers
```py
random_integers_between_50_and_100 = np.random.randint(low=50, high=101, size=(6))
#will generate 6 numbers in a range of (50 - 99 )
random_floats_between_0_and_1 = np.random.random([6])
#will create 6 numbers within a range of (0 - 1)
```
### Broadcasting
You can multiply and sum vectors or matrices with a scalar.
## Pandas gold concepts
Create a dataframe
```py 
#We need data and columns, where the need to match the number of columns
data = np.array([[1,2],[3,4],[5,6],[7,8],[9,10])
columns = ["temperature", "activity"]
df = pd.DataFrame(data= data, columns = columns)
```
`.iloc[ rows, columns ]`:Is similar as slicing but applied to the dataframe
`.loc[ filter_expression , column_name ]`: Filter
`.head( rows_number )`: print the first rows_number
`.copy()`: Creates a copy of the DF, because *=* only creates a reference.
```py
newData = oldData.copy()
#creates a copy, and it's not by reference.
```
