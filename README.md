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
3]**reverse the vowels in string**

s=input()
vowels="a,e,i,o,u,A,E,I,O,U"
s=list(s)
vowels_list=[char for char in s if char in vowels ]
vowels_list.reverse()
j=0
for i in range(len(s)):
    if s[i] in vowels:
       s[i]=vowels_list[j]
       j+=1
    else:
        s[i]=s[i]
print("".join(s))
