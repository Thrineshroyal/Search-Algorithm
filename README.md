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
Developed by: P.Jeshwanth Kumar
RegisterNumber: 212223230226
'''
def linearSearch(array,n,k):
    for i in range(0,n):
        if (array[i]==k):
            return i
    return -1
    
    
array = eval(input())
array.sort()
n=len(array)
# sort the array
k = eval(input()) # k-item to be seared for
# get the length of array and store in the variable n
result = linearSearch(array,n,k)# use the function for linear search
# use if-else to print sorted array and "Element not found" if the item is not present in the list otherwise print sorted array and "Element found at index: ", result
if result==-1:
    print(array)
    print("Element not found")
else:
    print(array)
    print("Element found at index: ",result)



```
ii)	# Find the element in a list using Binary Search(Iterative Method).
```
''' 
Program to find the element in a list using Binary Search(Iterative Method)..
Developed by: TANGUTURI THRINESH ROYAL
RegisterNumber: 212223230226
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
    
array = eval(input())
array.sort()
k = eval(input())
result=binarySearchIter(array,k,0,len(array)-1)
if result==-1:
    print(array)
    print("Element not found")
else:
    print(array)
    print("Element found at index: ",result)
```
iii)	# Find the element in a list using Binary Search (recursive Method).
```
''' 
Program to find the element in a list using Binary Search (recursive Method).
Developed by: TANGUTURI THRINESH ROYAL
RegisterNumber: 212223230226
'''
def BinarySearch(arr, k, low, high):
    while low<=high:
        mid=low+(high-low)//2
        if array[mid]==k:
            return mid
        elif array[mid]>k:
            return BinarySearch(array,k,low,mid-1)
        else:
            return BinarySearch(array,k,mid+1,high)
    return -1
array = eval(input())
array.sort()
k = eval(input()) 
result=BinarySearch(array,k,0,len(array)-1)
if result==-1:
    print(array)
    print("Element not found")
else:
    print(array)
    print("Element found at index: ",result)
    

# use the binary search function to find the result

# use if-else to print sorted array and "Element not found" if the item is not present in the list otherwise print sorted array and "Element found at index: ", result

```
## Output
i.Use a linear Search method to match the item in a list
![Screenshot 2023-12-29 221603](https://github.com/Thrineshroyal/Search-Algorithm/assets/145741928/d1505c24-3092-43b0-8f1b-597e59affed7)

ii.Find the element in a list using Binarysearch(Iterative Method)
![Screenshot 2023-12-29 221631](https://github.com/Thrineshroyal/Search-Algorithm/assets/145741928/323b8d78-af21-49f1-82ee-7820f36fcfd0)

iii.Find the element in a list using BinarySearch (recursive Method)
![Screenshot 2023-12-29 221657](https://github.com/Thrineshroyal/Search-Algorithm/assets/145741928/18858247-5fb2-4063-a14b-bb1a1e9731cd)

## Result
Thus the linear search and binary search algorithm is implemented using python programming.
