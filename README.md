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
```
''' 
Program for linear search method to match the item in a list
Developed by: Joel John Jobinse
RegisterNumber: 23008174
'''
def linearSearch(array,n,k):
    # write your code for linear search
    array.sort()
    print(array)
    index=0
    for i in range(1,n+1):
        if array[i]==k:
            index+=i
    if index==0:
        print("Element not found")
    else:
        print("Element found at index: ",index)
    
array = eval(input())
# sort the array
k = eval(input()) # k-item to be seared for
# get the length of array and store in the variable n
result = linearSearch(array,len(array)-1,k)# use the function for linear search
# use if-else to print sorted array and "Element not found" if the item is not present in the list otherwise print sorted array and "Element found at index: ", result


```
ii)	# Find the element in a list using Binary Search(Iterative Method).
```
''' 
Program to find the element in a list using Binary Search(Iterative Method)..
Developed by: Joel John Jobinse
RegisterNumber: 23008174
'''
def binarySearchIter(array, k, low, high):
    # Write your code here to find the middle value and check if the desired item is above or below the middle value
    while high>=low:
        mid=low+(high-low)//2
        if mid==k:
            return array.index(mid)
        elif mid<k:
            low=mid+1
        elif mid>k:
            high=mid-1
    return -1
    
array = eval(input())
# sort the array
array.sort()
low=array[0]
high=array[-1]
k = eval(input()) #k-item to be searched

result = binarySearchIter(array,k,low,high)# use the binary search function to find the item in the list
print(array)
if result != -1:
    print("Element found at index: ", result)
else:
    print("Element not found")
# use if-else to print sorted array and "Element not found" if the item is not present in the list otherwise print sorted array and "Element found at index: ", result

```
iii)	# Find the element in a list using Binary Search (recursive Method).
```
''' 
Program to find the element in a list using Binary Search (recursive Method).
Developed by: Joel John Jobinse
RegisterNumber: 23008174
'''
def BinarySearch(arr, k, low, high):
    # Write your code here for binary search using recursive method
    while high>=low:
        mid=low+(high-low)//2
        if mid==k:
            return arr.index(mid)
        elif mid<k:
            low=mid+1
            return BinarySearch(arr, k, low, high)
        elif mid>k:
            high=mid-1
            return BinarySearch(arr, k, low, high)
    return -1
    
arr = eval(input())
#sort the array
arr.sort()
low=arr[0]
high=arr[-1]
k = eval(input()) # k is the element to be searched for

result = BinarySearch(arr,k,low,high)# use the binary search function to find the result
if result != -1:
    print(arr)
    print("Element found at index: ", result)
else:
    print(arr)
    print("Element not found")
# use if-else to print sorted array and "Element not found" if the item is not present in the list otherwise print sorted array and "Element found at index: ", result
```
## Sample Input and Output
![linearsearch](https://github.com/joeljohnjobinse/Search-Algorithm/assets/138955488/86dc2f9f-82c6-4569-9808-5b65ee70f39d)
![binarysearch](https://github.com/joeljohnjobinse/Search-Algorithm/assets/138955488/704c78f1-b404-4ede-a9b6-c1170c9173ed)
![binarysearchrec](https://github.com/joeljohnjobinse/Search-Algorithm/assets/138955488/a93c6c98-a8d8-4273-9a37-2314c8efcaa7)


## Result
Thus the linear search and binary search algorithm is implemented using python programming.
