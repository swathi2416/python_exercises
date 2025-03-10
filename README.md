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
2]**harshad number**
def harshad(num):
    temp=num
    sum=0
    while(temp>=1):
        b=temp%10
        sum+=b 
        temp//=10
    if (num%sum)==0:
        return True
    else:
        return False
num=int(input("enter the number "))

print(harshad(num))
