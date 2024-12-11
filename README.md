perct_lst = []
n = int(input("Enter number of percentage: "))
for i in range(0, n):
    ele = float(input("Enter each percantage of student "))
    perct_lst.append(ele)
print(perct_lst)
 
#a) inSelection Sort
def insertionSort(list):
    for i in range(1, len(list)):
        a = list[i]
        j =  i- 1
        while j >= 0 and a < list[j]:
           list[j + 1] = list[j]
           j = j - 1
        list[j + 1] =a
        print (list)
newlist=(perct_lst)
insertionSort(newlist)
print("Sorted percentage list in Ascending Order:",newlist)
 
# b) Shell Sort and display top five scores
def shell_sort(arr):
    n = len(arr) // 2
    while n > 0:
        for i in range(n, len(arr)):
            temp = arr[i]
            j = i
            while j >= n and arr[j - n] > temp:
                arr[j] = arr[j - n]
                j -= n
                print(arr)
            arr[j] = temp
        n //= 2
 
arr =(perct_lst)
shell_sort(arr)
print(" Shell Sort ", arr)
