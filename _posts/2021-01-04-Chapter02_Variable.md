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


## 3. 리터럴(literal)
--- 

  원래 12,123,3.14, 'A' 와 같은 값들이 '상수'인데 프로그래밍에서는 상수를 값으  한 번 저장하면 변경할 수 없는 저장공간으로 정의하기때문에 위의 상수와 다르게 불러야만 해서 **리터럴**이라는 용어를 사용한다. 


  - **변수(Variable)**  하나의 값을 저장하기 위한 공간

  - **상수(Constant)**  값을 한번만 저장할 수 있는 공간

  - **리터럴(Literal)**  그 자체로 값을 의미하는 것
  

```css
    final int MAX_VALUE; //정수형 상수 선언
    MAX_VALUE = 100;     //처음 값 저장
    MAX_VALUE = 200;     //에러, 상수에 저장돈 값을 변경할 수 없음
    
```

#### 4. 리터럴의 타입과 접미사

  정수형과 실수형에는 여러 타입이 존재하므로, 리터럴에 접미사를 붙여서 타입을 구분한다. 
<mark> long 타입의 경우 접미사 'l' 또는 'L' </mark> 을 붙이고, 접미사가 없으면 int 타입의 리터럴이 된다. 



<table class="tg">
<thead>
  <tr>
    <th class="tg-amwm">종류</th>
    <th class="tg-amwm">리터럴</th>
    <th class="tg-amwm">접미사</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">논리형</td>
    <td class="tg-0lax">false, true</td>
    <td class="tg-0lax">없음</td>
  </tr>
  <tr>
    <td class="tg-tpo9">정수형</td>
    <td class="tg-tpo9">123, 0b0101, 077, 0xFF, 100L</td>
    <td class="tg-tpo9"><span style="font-weight:bold">L</span></td>
  </tr>
  <tr>
    <td class="tg-tpo9">실수형</td>
    <td class="tg-tpo9">3.14, 3.0e8, 1.4f, 0x1.0p-1</td>
    <td class="tg-tpo9"><span style="font-weight:bold">f</span>, d</td>
  </tr>
  <tr>
    <td class="tg-0lax">문자형</td>
    <td class="tg-0lax">'A', '1', '/n'</td>
    <td class="tg-0lax">없음</td>
  </tr>
  <tr>
    <td class="tg-0lax">문자열</td>
    <td class="tg-0lax">"ABC", "1234", "A", "true"</td>
    <td class="tg-0lax">없음</td>
  </tr>
</tbody>
</table>


```css
int oct = 010;      //8진수 10, 10진수의 8
int hex = 0x10;     // 16진수의 10, 10진수로 16
```
8진수는 앞에'0' 을 붙이고 16진수는 리터럴 앞에 <mark>접두사 '0x' 또는 '0X' </mark>를 붙인다.


```css
long big = 100_000_000_000L;
long hex = 0xFFFF_FFFF_FFFF_FFFFL;
```
JDK1.7부터는 중간에 <mark>구분자 '_'</mark>를 넣을 수 있게 되었다.


```css
float pi = 3.14f;     //접미사f 대신 F 사용가능 , 생략불가
double rate = 1.619d; //접미사d 대신 D 사용가능 , 생략가능
```
<mark> float 타입은 'f' </mark>를 붙이지 않으면 default double 타입이 된다. 