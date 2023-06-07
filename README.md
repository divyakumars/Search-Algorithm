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
Developed by:DIVYA K
RegisterNumber: 212222230035
'''
def linearSearch(array,n,k):
    for i in range(0,n):
        if array[i]==k:
            return i
    return -1    
array = eval(input())
k = eval(input())
n=len(array)
array.sort()
result = linearSearch(array,n,k) # use the function for linear search
if (result==-1):
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
Developed by:DIVYA K
RegisterNumber: 21222230035
'''
def BinarySearchIter(array, k, low, high):
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
result=BinarySearchIter(array,k,0,len(array)-1)
if(result==-1):
    print(array)
    print("Element not found")
else:
    print(array)
    print("Element found at index: ",result)
```
iii)	# Find the element in a list using Binary Search (recursive Method)
```
''' 
Program to find the element in a list using Binary Search (recursive Method).
Developed by: DIVYA K
RegisterNumber: 212222230035
'''
def BinarySearch(arr, k, low, high):
    if high>=low:
        mid=low+(high-low)//2
        if array[mid]==k:
           return mid
        elif array[mid]<k:
            return BinarySearch(array,k,mid+1,high)
        else:
            return BinarySearch(array,k,low,mid +1)
    return -1
  
array = eval(input())
array.sort()
print(array)

k = eval(input()) # k is the element to be searched for
low=0
high=len(array)-1
result=BinarySearch(array,k,low,high)
if result>=0:
    print("Element found at index: " ,result)
else:
    print("Element not found")




```
## Sample Input and Output
![image](https://github.com/divyakumars/Search-Algorithm/assets/119393621/4b4afde2-fbb6-4104-bf90-38612cec6164)

![image](https://github.com/divyakumars/Search-Algorithm/assets/119393621/794311aa-2e15-45de-8847-601242a7fbd3)


![image](https://github.com/divyakumars/Search-Algorithm/assets/119393621/5be25404-c0a5-4737-a94b-69af3749d6d4)


## Output
![image](https://github.com/divyakumars/Search-Algorithm/assets/119393621/4477015b-3133-43f5-881f-0ff928efff75)

![image](https://github.com/divyakumars/Search-Algorithm/assets/119393621/d601dc5f-02c6-452f-8225-9c36353a4747)

![image](https://github.com/divyakumars/Search-Algorithm/assets/119393621/82cc807b-2b1a-44b9-851e-ec9276997bb2)



## Result
Thus the linear search and binary search algorithm is implemented using python programming.
