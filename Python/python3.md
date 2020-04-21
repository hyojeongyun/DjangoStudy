# 파이썬 스터디
Module
-------
링크 : <https://docs.python.org/3/library/index.html>
```python
import math  # math라는 이름의 모듈 가져옴
print(math.ceil(2.1))  # 올림 3
print(math.floor(2.9)) # 내림 2
print(math.sqrt(4))  # 제곱근 2
```
---
egoing.py
```python
def a():
   return 'a'
def b():
   return 'b'
```
k8805.py
```python
def a():
   return 'B'
```
1.py
```python
from egoing import a  # egoing 이라는 모듈로부터 a라는 함수만 import
import k8805  # 모듈을 import
print(a())  # a 출력
print(k8805.a())  # B 출력
```
