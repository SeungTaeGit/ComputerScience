# 목표
자바 소스 파일(.java)을 JVM으로 실행하는 과정 이해하기

## 학습할 것
* JVM이란 무엇인가
* 컴파일 하는 방법
* 실행하는 방법
* 바이트코드란 무엇인가
* JIT 컴파일러란 무엇이며 어떻게 동작하는지
* JVM 구성 요소
* JDK와 JRE의 차이
<br>


### * JVM이란 무엇인가
---
  - JVM(Java Virtual Machine) 자바 가상 머신을 줄여 부르는 용어이다.
  - OS와 JAVA Application 사이에서 중재자 역할을 한다.
  - 자바 컴파일러에 의해 바이트 코드로 변환된 자바 소스 파일을 클래스 로더를 통해 읽어 자바 API와 함께 실행한다.
<br>
> **- 왜 사용할까?** <br><br>
>   모든 프로그래밍 언어는 application(source) -> compilered source -> OS -> Hardware 의 구조를 가진다.<br>
>   위 구조의 경우 사용하는 OS에 따라 코드해석을 달리 해야한다.<br>
>    -> java의 경우 JVM을 사용, 자바 바이트코드(.class)파일을 실제 사용중인 OS에 맞는 특화된 코드로 변환하여 실행한다.
<br>


### * 컴파일 하는 방법
---
  - Compile : 사람이 읽기 쉬운 소스 코드를 컴퓨터가 읽기 쉽게 변환해주는 개념.
  - Java 컴파일의 경우 사람이 작성한 프로그래밍 코드를 JVM이 이해할 수 있는 수준으로 변환하는 작업.

  
<br>


### 3. 실행하는 방법
---
<br>


### 4. 바이트코드란 무엇인가
---
<br>


### 5. JIT 컴파일러란 무엇이며 어떻게 동작하는지
---
<br>


### 6. JVM 구성 요소
---
  <p align="center"><img src="https://github.com/SeungTaeGit/ComputerScience/assets/129585999/b157e002-c26b-467e-a655-0373e0f70652"></p>
<br>


### 7. JDK와 JRE의 차이
---

