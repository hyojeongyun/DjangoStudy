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
