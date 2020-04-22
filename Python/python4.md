# 파이썬 스터디

객체 지향 프로그래밍
-------------------
object = class + instance
* 클래스 정의

  ```python
  class cal(object):
  ```
* 생성자

  ```python
  def __init__(self, v1, v2):
  ```
* instance 변수와 method
  * method의 첫번째 매개변수는 꼭 정의해야함.
  
  * instance 생성될 때 생성한 instance(관습적으로 ```self```)가 생성자의 첫번째 매개변수로 들어감.

  * 첫번째 매개변수를 이용해서 instance의 변수 지정.
  ```python
  class Cal(object):
    def __init__(self, v1, v2):
      self.v1=v1
      self.v2=v2
   def add(self):
     return self.v1 + self.v2
    def subtract(self):
     return self.v1 - self.v2
    
  c1 = Cal(30,20)
  print(c1.add())  # 50 출력
  print(c1.subtract())   # 10 출력
  ```

캡슐화
------
  * method 바깥에서 instance 변수에 직접 접근하는 것 허용
    
    객체를 사용하는 사람이 올바르게 사용할 것이라 가정
  
  * set / get method
    
    ```python
     class Cal(object):
        def __init__(self, v1, v2):
            if isinstance(v1, int):
               self.v1 = v1
            if isinstance(v2, int):
               self.v2 = v2
       def add(self):
            return self.v1 + self.v2
       def subtract(self):
           return self.v1 - self.v2
       def setV1(self, v):
            if isinstance(v, int):  # v 가 int 인지 확인
                self.v1 = v
        def getV1(self):
            return self.v1
        
    c1 = Cal(10,10)
    print(c1.add())  # 20 출력
    print(c1.subtract())  # 0 출력
    c1.setV1('one')
    c1.v2 = 30
    print(c1.add())  # 40 출력
    print(c1.subtract())  # -20 출력
  
  
  * 변수 이름 앞에 ```__``` 붙이면 instance 외부에서 접근 금지. 내부에선 접근 가능.
  
    ```python
    class C(object):
      def __init__(self, v):
        self.__value = v
      def show(self):
        print(self.__value)
        
    c1 = c(10)
    print(c1.__value)  # 에러
    c1.show()  # 10 출력
    ```
  

상속
----
* object 대신에 상속할 class 이름 넣음. 

  ```python
  class class2(class1):
  ``` 
* 자식 class 생성자 없으면 부모 class 생성자로

* 부모 객체의 변수도 상속받음.

  ```python
  class CalMultiply(Cal):
    def multiply(self):
        return self.v1 * self.v2
  class CalDivide(CalMultiply):
    def divide(self):
        return self.v1 / self.v2
        
  c1 = CalMultiply(10,10)
  print(c1.add())  # 20 출력
  print(c1.multiply())  # 100 출력
  c2 = CalDivide(20,10)
  print(c2.add())  # 30 출력
  print(c2.multiply())  # 200 출력
  print(c2.divide())  # 2.0 출력
  ```
  
클래스 멤버
-----------
#### 클래스 메소드
  * static method
    * @staticmethod
    * class 소속
    
  * class method
    * @classmethod
    * class 소속
    * 첫번째 인자로 메소드가 소속되어 있는 클래스를 가르키는 값 들어옴
    
  * instance method
    * instance 소속
    
  ```python
  class Cs:
    @staticmethod
    def static_method():
      print("Statkc method")
    @classmethod
    def class_method(cls):
      print("Class method")
    def instance_method(self):
      print("Instance method")
      
  i = Cs()
  Cs.static_method()
  Cs.class_method()
  i.instance_method()
  ```
#### 클래스 변수 
 * 모든 instance가 같은 저장공간 공유
 * 클래스의 안, 메소드의 밖인 곳에 변수 선언하면 그 변수는 클래스에 소속된 클래스 변수가 됨
 * 클래스의 안, 메소드의 밖에서 정의할 때 ```클래스이름.``` 붙이지 않음
 * 메소드의 안에서 클래스 변수에 접근 할 때 ```클래스이름.``` 붙여야 함
 * 변수 이름 앞에 ```_``` 붙이면 외부접근 불가
 
Override
--------
  자식객체가 부모객체(super 객체)의 메소드 재정의
  ```python
  class C1:
   def m(self):
     return 'parent'
  class C2(C1):
   def m(self):     # override
     return super().m() + ' child'    
      
  o = C2()
  print(o.m())  # parent child 출력
  ```
  
객체와 모듈
----------
  1.py
  
  ```python
  import lib
  obj = lib.A()
  print(obj.a())  # 
  ```
  lib.py
  ```python
  class A:
    def a(self):
      return 'a'
  ```
다중상속
--------
  자식이 상속받는 부모 클래스가 여러 개
  
  단점 있음
  ```python
  class C1():
    def c1_m(self):
      print("c1_m")
    def m(self):
      print("C1 m")
      
  class C2():
    def c2_m(self):
      print("c2_m")
    def m(self):
      print("C2_m")
      
  class C3(C2, C1):
    def m (self):
      print("C3 m")
      
  c = C3()
  c.c1_m()  # c1_m 출력
  c.c2_m()  # c2_m 출력
  c.m()   # C1 에도 m 있고 C2에도 m 있고 C3에도 m 있음
          # 원하는대로 동작하지 않을 확률 높음
  print(c3.__mro__)  # 부모 클래스의 우선순위 정보 출력
  ```
