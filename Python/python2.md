# 파이썬 스터디
List
----
```python
print(type('egoing')) # <class 'str'> 출력
pring(type(['egoing', 'leezche', 'graphittie'])) # <class 'list'> 출력

names = ['egoing', 'leezche', 'graphittie']
print(names) # ['egoing', 'leezche', 'graphittie'] 출력
print(names[2]) # graphittie 출력

 # 하나의 List에 다양한 형태의 Data 들어갈 수 있음
egoing = ['programmer', 'seoul', 25, False]
egoing[1] = 'busan'
print(egoing) # ['programmer', 'busan', 25, False] 출력
```
List 심화
---------
```python
names = ['A', 'B', 'C']
'A' in names # True
'D' in names # False

nums = [1, 100, 12312312]
nums.reverse() # 순서 반대로
print(nums) # [12312312, 100, 1] 출력

al = ['A','B','C','D']
print(len(al)) # 4 출력
al.append('E') # al 끝에 'E'추가
print(al) # ['A', 'B', 'C', 'D', 'E'] 출력
del(al[0]) # al 첫번째 원소 삭제
print(al) # ['B', 'C', 'D', 'E'] 출력
```
while
------
```python
# Hello World 3번 출력
i = 0;
while i < 3:
   print('Hello world')
   i = i + 1
```
```python
i = 0
while i < 10:
   print('print("Hello World '+ str(i*9)+ '")')
   i = i + 1
```
```python
i = 0
while i < 10:
   if i == 4:
      print(i) # i == 4 일때만 i 출력
   i = i + 1
```
```python
i = 0
while i < 10:
   if i == 4:
      break
   print(i)
   i = i + 1
print('after while') # 0부터 3까지 출력 후 after while 출력
```
List & while
------------
```python
members = ['egoing', 'leezche', 'graphittie']
i = 0
while i < len(members):
      print(members[i])
      i = i + 1
# egoing 출력
# leezche 출력
# graphittie 출력
```
For
---
```python
members = ['egoing', 'leezche', 'graphittie']
# list 안에 있는 값 반복문 실행될 때마다 꺼내서 in 앞에 있는 변수에 담음
for member in members:  
   print(member)
```
```python
for item in range(5):
   print(item)
# 0 1 2 3 4 출력
```
```python
for item in range(5, 11):
   print(item)
# 5 6 7 8 9 10 출력
```
```python
input_id = input("아이디를 입력해주세요.\n")
members = ['egoing', 'k8805', 'leezche']
for member in members:
   if member == input_id:
       print('Hello!, '+member)
       import sys
       sys.exit()   # 프로그램 끝냄
print('who are you?')
```
Function
--------
```python
def a3():
   print('aaa')
a3()  # aaa 출력
```
---
* 리턴값
```python
def a3():
   return 'aaa'
print(a3()) # aaa 출력
```
---
* 입력값
```python
def a(num):
   return 'a'*num
print(a(3))  # aaa 출력
```
```python
def make_string(str, num):
   return str*num
print(make_string('b', 3)) # bbb 출력
```
---
```python
input_id = input("아이디를 입력해주세요.\n")
def login(_id):
   members = ['egoing', 'k8805', 'leezche']
   for member in members:
      if member == _id:
         return True
   return False
if login(input_id):
   print('Hello, '+input_id)
else:
   print('Who are you?')
```
