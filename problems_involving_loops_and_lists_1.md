# Loops and Arrays Set 1

##### Problem statements by Robert Kim

---

**(Lists are the same thing as Arrays!)**  

### 1. Largest Integer

Return the largest integer in an array.

#### Code

~~~python
# arr is an array with only positive integers.
# @return: the largest element in arr.
def largest_int(arr):
	# code here
~~~

#### Examples

~~~python
arr = [1, 3, 5, 2, 3, 5, 10, 1, 3]
largest_int(arr) # returns 10
~~~

~~~python
arr = [1, 3, 4, 1, 4, 4]
largest_int(arr) # returns 4
~~~

<div style="page-break-before: always !important"></div>

### 2. Linear Search

Linear search is an algorithm for finding if a number, the key, is in an array or not. It returns the index of the key if it is in the array, otherwise it will return -1 to indicate that it is not in the array.

#### Code

~~~python
# arr is a array with only unique integers.
# key is a value that you want to find in the array.
# @return: the index of the key if it is in the array, otherwise -1.
def linear_search(arr, key):
	#code here
~~~

#### Examples

~~~python
arr = [1, 4, 6, 2, 3, 7, 8, 9]
key = 4
linear_search(arr, key) # returns 1
~~~

~~~python
arr = [1, 2, 6, 4, 8, 19, 3, 5]
key = 19
linear_search(arr, key) # returns 5
~~~

~~~python
arr = [3, 2, -1, 5, 6]
key = 0
linear_search(arr, key) # returns -1
~~~

~~~python
lst = []
key = 4
linear_search(lst, key) # returns -1
~~~

<div style="page-break-before: always !important"></div>

### 3. Categorization (Challenge)

Categorization involves taking a larger set of data and categorizing them into smaller sub-sets. In computer science, there is a concept of multi-dimensional arrays. Basically, it is just arrays inside of arrays. In Python, it might look like this:

~~~python
a = [1, 2, 3] # a is a 1-dimensional array
b = [4, 5, 6]
c = [7, 8, 9]
d = [a, b, c] 
# d is [[1, 2, 3], 
#       [4, 5, 6], 
#       [7, 8, 9]], a two-dimensional array
# d[0] returns [1, 2, 3]
~~~

For this problem, given a one-dimensional array, categorize it so that even numbers are in one sub-set and odd numbers are in another. You will need to use a function of arrays called ```append()``` which adds an element to the end of an array. It works like this:

~~~python
a = [2]
a.append(1) # a is now [2, 1]
b = [[2, 3], [1, 4]]
b[0].append(1) # b is now [[2, 3, 1], [1, 4]]
~~~

For this problem, odd numbers should go in a sub-array and even numbers should go in another sub-array of a larger array.

#### Code

~~~python
# arr is an array of only integers.
# @return: a two-dimensional array with one sub-array containing odd numbers and another 
#          sub-array containing even numbers.
# hint: use the append() function on the sub-arrays of temp!
def categorize(arr):
	temp = [[], []]
	# code here
	return temp
~~~

**Examples on the next page.**

<div style="page-break-before: always !important"></div>

**Continued from problem 3 on the last page.**

#### Examples

~~~python
arr = [1, 2, 5, 3, 5, 2, 3, 4, 6, 7]
categorize(arr) # returns [[1, 5, 3, 5, 3, 7], [2, 2, 4, 6]]
~~~

~~~python
arr = [4, 5, 2, -1, 0, 2, -19, 3, 2, 56, 7, 3, 2]
categorize(arr) # returns [[5, -1, -19, 3, 7, 3], [4, 2, 0, 2, 2, 56, 2]]
~~~

~~~python
arr = []
categorize(arr) # returns [[], []]
~~~