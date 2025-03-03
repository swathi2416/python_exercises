# python_exercises
1]**rotate left**
def left_rotate(arr,k):
    n=len(arr)
    k=k%n
    temp=arr[:k]
    for i in range(n-k):
        arr[i]=arr[i+k]
    arr[-k:]=temp
    
        

arr=list(map(int,input().split()))
k=int(input())
left_rotate(arr,k)
print(arr)
