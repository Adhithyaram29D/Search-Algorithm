# Linear Search and Binary search
## Aim:
To write a program to perform linear search and binary search using python programming.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
## Linear Search:
1.	Start from the leftmost element of array[] and compare k with each element of array[] one by one.
2.	If k matches with an element in array[] , return the index.
3.	If k doesn’t match with any of elements in array[], return -1 or element not found.
## Binary Search:
1.	Set two pointers low and high at the lowest and the highest positions respectively.
2.	Find the middle element mid of the array ie. arr[(low + high)/2]
3.	If x == mid, then return mid.Else, compare the element to be searched with m.
4.	If x > mid, compare x with the middle element of the elements on the right side of mid. This is done by setting low to low = mid + 1.
5.	Else, compare x with the middle element of the elements on the left side of mid. This is done by setting high to high = mid - 1.
6.	Repeat steps 2 to 5 until low meets high
## Program:
i)	#Use a linear search method to match the item in a list.
```python
''' 
Program for linear search method to match the item in a list
Developed by: ADHITHYARAM D
RegisterNumber: 212222230008
'''
def linearSearch(array,n,k):
    for i in  range(0,n):
        if(array[i]==k):
            return i
    return -1        
    
array = eval(input())
# sort the array
k = eval(input()) # k-item to be seared for
# get the length of array and store in the variable n
n=len(array)
array.sort()
result = linearSearch(array,n,k)# use the function for linear search
# use if-else to print sorted array and "Element not found" if the item is not present in the list otherwise print sorted array and "Element found at index: ", result
if(result==-1):
    print(array)
    print("Element not found")
else:
    print(array)
    print("Element found at index: ",result)
```
ii)	# Find the element in a list using Binary Search(Iterative Method).
```python
''' 
Program to find the element in a list using Binary Search(Iterative Method)..
Developed by: ADHITHYARAM 
RegisterNumber: 212222230008 
'''
def binarySearchIter(array, k, low, high):
    while low<=high:
        mid=low+(high-low)//2
        if array[mid]==k:
            return mid
        elif array[mid]<k:
            low=mid+1
        else:
            high=mid-1
            
    return -1
    # Write your code here to find the middle value and check if the desired item is above or below the middle value
    
    
array = eval(input())
# sort the array
array.sort()
k = eval(input()) #k-item to be searched

# use the binary search function to find the item in the list
result=binarySearchIter(array,k,0,len(array)-1)
# use if-else to print sorted array and "Element not found" if the item is not present in the list otherwise print sorted array and "Element found at index: ", result
if result==-1:
    print(array)
    print("Element not found")
else:
    print(array)
    print("Element found at index: ",result)
```
iii)	# Find the element in a list using Binary Search (recursive Method).
```python
''' 
Program to find the element in a list using Binary Search (recursive Method).
Developed by: ADHITHYARAM D
RegisterNumber: 212222230008
'''
def BinarySearch(array, k, low, high):
    if high>=low:
        mid=low+(high-low)//2
        if array[mid]==k:
            return mid
        elif array[mid]>k:
            return BinarySearch(array,k,low,mid-1)
        else:
            return BinarySearch(array,k,mid+1,high)
    else:        
        return -1    
array = eval(input())
array.sort()
#sort the array
k = eval(input()) # k is the element to be searched for
result=BinarySearch(array,k,0,len(array)-1)
if result==-1:
    print(array)
    print("Element not found")
else:
    print(array)
    print("Element found at index: ",result)

```
## Output
![Screenshot 2023-06-03 215838](https://github.com/Adhithyaram29D/Search-Algorithm/assets/119393540/62af6068-9097-4115-b4cf-ffb24c923a78)

![Screenshot 2023-06-03 215908](https://github.com/Adhithyaram29D/Search-Algorithm/assets/119393540/4ccf7c06-f766-47cf-9a02-46032bebd4ef)

![Screenshot 2023-06-03 215941](https://github.com/Adhithyaram29D/Search-Algorithm/assets/119393540/3431bb71-07ac-4460-8c77-e2f586b19af3)

## Result
Thus the linear search and binary search algorithm is implemented using python programming.
