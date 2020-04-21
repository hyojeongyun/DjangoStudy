# 파이썬 스터디

Hello World
-----------
```python
print("Hello World!")
```
Math
----
```python
print(10+5) # 15 출력
print(10-5) # 5 출력
print(10*5) # 50 출력
print(10/5) # 2.0 출력
```
---
```python
import math
print(math.ceil(2.2))  # 3 출력
print(math.floor(2.7)) # 2 출력
print(math.pow(2,10)) # 1024 출력
print(math.pi) # 파이 출력
```
String
------
```python
print('Hello')
print("Hello")
print("Hello 'world'") # Hello 'world' 출력
print('Hello "world"') # Hello "world" 출력

print('Hello '+'world') # Hello world 출력
print('Hello '*3) # Hello Hello Hello 출력
print('Hello'[0]) # H
print('Hello'[1]) # e
print('Hello'[2]) # l
```
---
```python
print('hello world'.capitalize()) # Hello world
print('hello world'.upper()) # HELLO WORLD
print('Hello world'.__len__()) # 11
print(len('hello world')) # 11
print('Hello world'.replace('world', 'programming')) # Hello programming

print("egoing's \"tutorial\"")
print("\\") # \
print("Hello \nworld") # 개행
print("Hello \t\tworld") # Hello   World
print("\a") # 알림음
print(10+5) # 15 출력
print("10"+"5") # 105 출력
```
Variable
--------
```python
x=10
y=5
print(x+y)

title = "python & ruby"
print("Title is "+title)

name = "이상효"
print("안녕하세요. "+name+"님")
print(name+"님을 위한 강의를 준비했습니다.")
print(name+"님 꼭 참석 부탁드립니다.")

donation=200
student=10
sponsor=100
print((donation*student)/sponsor)
```
Boolean
-------
```python
a=1 
b=1
print(a==b) # True
print(1==2) # False
print(1>2) # False
print(1<2) # True
print(True) # True
print(False) # False
```
if & if else & else
-------------------
```python
input=33
real_egoing =11
real_k8805="ab"
if real_egoing == input:
  print("Hello!, egoing")
elif real_k8805==input:
  print("Hello!, k8805")
else:
  print("Who are you?")  # Who are you 출력
```
Input
-----
```python
in_str = input("입력해주세요.\n")
print(in_str.upper()+" World!") #(입력값) World! 출력
```
AND & OR & NOT
--------------
* AND : ```and```
* OR : ```or```
* NOT : ```not```
