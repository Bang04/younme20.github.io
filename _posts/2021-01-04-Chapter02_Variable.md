---
layout: post
title: "Chapter02. 변수"
description: "자바의 기본 핵심을 요약 설명 해준다."
date: 2021-01-04
tags: [JAVA, ]
comments: true
share: false
---

---

## 1. 화면에 글자 출력하기
---

```css
    System.out.print();   줄바꿈을 하지 않는다.
    System.out.println(); 줄바꿈을 한다.

    System.out.println("3+5");  3+5 출력
    System.out.println(3+5);    8  출력
```
    


## 2. 변수 (vriable)란?
--- 

#### 1. 변수의 선언과 저장

저장공간, 즉 변수가 필요하다면 먼저 변수를 선언해야한다. 

```css
    int x; //변수의 선언   
    x = 5; //변수에 대입

    int x = 5; //한 줄로 표현
```

#### 2. 변수의 타입

<!-- | 분류    | 변수의 타입         | 설명          |
| :------ | :----------------: | ------------------------------------------------------------------: |
| 숫자    | int, **long**       |정수(integer)를 저장하기 위한 타입(20억이 넘을땐 long)                 |
|         | float, **double**   |실수(floating-point number)를 저장하기 위한 타입<br>(float 는 오차없이 7자리, double은 15자기)|
| 문자    | char                |문자(character)를 저장하기 위한 타입                                  |
|         | String              |여러 문자(문자열, string) 를 저장하기 위한 타입                        | -->

<table class="tg">
<thead>
  <tr>
    <th class="tg-0pky">분류</th>
    <th class="tg-0pky">변수의 타입</th>
    <th class="tg-c3ow">설명</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0pky" rolspan=2>숫자</td>
    <td class="tg-0pky"><span style="font-weight:bold">int </span><br>long</td>
    <td class="tg-0pky">정수(integer)를 저장하기 위한 타입(20억이 넘을땐 long)</td>
  </tr>
  <tr>
    <td class="tg-0pky"></td>
    <td class="tg-0pky">float<br><span style="font-weight:bold">double</span></td>
    <td class="tg-0pky">실수(floating-point number)를 저장하기 위한 타입<br>(float 는 오차없이 7자리, double은 15자기)</td>
  </tr>
  <tr>
    <td class="tg-0pky" rolspan=2>문자</td>
    <td class="tg-0pky">char</td>
    <td class="tg-0pky">문자(character)를 저장하기 위한 타입</td>
  </tr>
  <tr>
    <td class="tg-0pky"></td>
    <td class="tg-0pky">String</td>
    <td class="tg-0pky">여러 문자(문자열, string) 를 저장하기 위한 타입</td>
  </tr>
</tbody>
</table>

```css

    int x = 100;        //정수(Integer)를 저장할 변수의 타입은 int로 한다.
    double pi - 3.14;   //실수를 저장할 변수의 타입은 double로 한다.
    char ch = 'a'       //문자(1개)를 저장할 변수의 타입은 char로 한다.
    String str = "abc"; //여러 문자(0~n개)를 저장할 변수의 타입은 String 으로 한다.
```

#### 3. 상수와 리터럴
    상수는 변수와 마찬가지로 '값을 저장할 수 있는 공간'이지만 변수와 달리 한번 값을 저장하면 다른 값으로 변경할 수 없다. 단지 변수 타입 앞에 final을 붙여준다.

```css
    final int MAX_VALUE; //정수형 상수 선언
    MAX_VALUE = 100;     //처음 값 저장
    MAX_VALUE = 200;     //ERROE, 상수에 저장돈 값을 변경할 수 없음
    
```     
#### 4. 운영체제에 독립적
    자바 응용프로그램은 운영체제나 하드웨어가 아닌 JVM하고 통신하고 자바로 작성된 프로그램으로 전달 받은 명령을 해당
    운영체제가 이해할 수 있도록 변환하여 전달


## 3. 자바가 쓰이는 곳
 --- 
    -  PC, 웹, 모바일 애플리케이션
    -  빅데이터
    -  게임,과학,소형기기 등


## 4. 자바 가상 머신(JVM)이란?
--- 
    자바를 실행하기 위한 가상 컴퓨터라고 이해 하면 쉽다.


## 5. 자바 개발도구(JDK)란?
--- 
    JDK(Java Development Kit)를 설치하면, JVM 과 자바 클래스 라이브러리 외 자바를 
    개발하는데 필요한 프로그램들이 설치된다. 


## JDK 설치순서
---
    1. [https://www.oracle.com/java/technologies/javase-downloads.html] 접속
    2. 사이트 접속하여 모든 쿠키 수락
    3. 라이센스 동의, 자신의 맞는 운영체제(64bit OR 32bit) 버전 클릭




## 6. 첫 번째 자바 프로그램 작성하기
--- 
1. javac.exe - 자바 컴파일러. 사람이 작성한 문장을 기계어로 번역 소스 파일(*.java) 을 클래스 파일(*.class)로 변환
2. java.exe - 자바 인터프리터. 자바 프로그램(class 파일)을  실행
3. 클래스 - 자바 프로그램의 단위. 자바 프로그램을 클래스들로 구성
    
    ```css
    class 클래스명 {

    }
    ```
4. main메서드 - 자바 프로그램의 시작점. 이메서드 없이 실행 불가.
    ```css
    public class array1 {
        public static void main(String[] args) {
        
        }
    }
     ```


## 7. 자바 API 란?
--- 
### Java API 란?
    Java로 프로그램을 만드는데 필요한 주요 기능을 미리 만들어서 
    제공하며 우리는 요청하는 방식으로 데이터만 던져서 원하는 결과
    값을 받을 수 있다.


### Java API 문서란?  
    Java API가 제공하는 기능에 대한 상세한 정보를 제공

- API 문서 링크
   [https://docs.oracle.com/javase/8/docs/api/index.html?help-doc.html]
 

