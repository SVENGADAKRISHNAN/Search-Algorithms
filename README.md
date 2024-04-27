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
def linearsearch(list,n,a):
    for i in range(0,n):#we iterate i to be the value of index
        if(list[i]==a):# for example at that particular index,the value is equal to the given value it reuturns that i valu
            return i
    return -1#if not it returns -1.WE GENERALLY USE -1.NOT FOUND MEANS -1.WE CAN USE ANY OTHER VALUE AS WELL 
list=eval(input())#getting the list
a=eval(input())#getting the value to be searched
n=len(list)#lenght of the list
list.sort()#sorting the list
result=linearsearch(list,n,a)#calling the function and passing three arguements
if(result==-1):
    print(list)
    print("Element not found")
else:
    print(list)
    print("Element found at index: ",result)


```
ii)	# Find the element in a list using Binary Search(Iterative Method).
```
def binary(array, key, low, high):
    while(low<=high):
        mid=low+(high-low)//2
        if array[mid]==key:
           return mid
        elif array[mid]<key:
           low=mid+1
        elif array[mid]>key:
           high=mid-1
    return -1
array=eval(input())
key=int (input())
array.sort ()
low, high=0, len (array)- 1
print(array)
result=binary(array,key,low,high)
if result==-1:
    print("Element not found")
else:
    print("Element found at index: ",result)




```
iii)	# Find the element in a list using Binary Search (recursive Method).
```
def binary(array,key,low,high):
    if high>=low:
        mid=low+(high-low)//2
        if array[mid]==key:
            return mid
        elif array[mid]<key:
            return binary(array,key,mid+1,high)
        elif array[mid]>key:
            return binary(array,key,low,mid-1)
    return -1
array=eval(input())
key=int(input())
array.sort()
low,high=0,len(array)-1
print(array)
result=binary(array,key,low,high)
if result==-1:
    print("Element not found")
else:
    print("Element found at index: ",result)




```
## Sample Input and Output

![pyhton exp 7,1](https://github.com/SVENGADAKRISHNAN/Search-Algorithms/assets/147473084/5d34a9e8-05fe-4775-9cfc-975c16175051)

![python exp7,2](https://github.com/SVENGADAKRISHNAN/Search-Algorithms/assets/147473084/19d4314a-8d01-4a84-9e36-3cab60d0feb5)

![python exp7,3](https://github.com/SVENGADAKRISHNAN/Search-Algorithms/assets/147473084/e23f0192-a1a6-48f1-94f1-700b9b0e4e8e)





## Result
Thus the linear search and binary search algorithm is implemented using python programming.
