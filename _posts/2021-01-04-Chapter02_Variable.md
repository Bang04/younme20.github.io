---
layout: post
title: "Chapter02. 변수"
description: "자바의 기본 핵심을 요약 설명 해준다."
date: 2021-01-12
tags: [print, Scanner, 상수, 리터럴  ]
comments: true
share: false
---

---

# Chapter2. 변수  (Variable)




#### 화면에 글자 출력하기
---

```css
    System.out.print();   줄바꿈을 하지 않는다.
    System.out.println(); 줄바꿈을 한다.

    System.out.println("3+5");  3+5 출력
    System.out.println(3+5);    8  출력
```
    


## 1. 변수 (vriable)란?
--- 

### 1. 변수의 선언과 저장

저장공간, 즉 변수가 필요하다면 먼저 변수를 선언해야한다. 

```css
    int x; //변수의 선언   
    x = 5; //변수에 대입

    int x = 5; //한 줄로 표현
```

### 2. 변수의 타입

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


## 2. 리터럴(literal)
--- 

  원래 12,123,3.14, 'A' 와 같은 값들이 '상수'인데 프로그래밍에서는 상수를 값으  한 번 저장하면 변경할 수 없는 저장공간으로 정의하기때문에 위의 상수와 다르게 불러야만 해서 **리터럴**이라는 용어를 사용한다. 


###  1. 상수와 리터럴
  - **변수(Variable)**  하나의 값을 저장하기 위한 공간

  - **상수(Constant)**  값을 한번만 저장할 수 있는 공간

  - **리터럴(Literal)**  그 자체로 값을 의미하는 것
  

```css
    final int MAX_VALUE; //정수형 상수 선언
    MAX_VALUE = 100;     //처음 값 저장
    MAX_VALUE = 200;     //에러, 상수에 저장돈 값을 변경할 수 없음
    
```

### 2. 리터럴의 타입과 접미사

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


8진수는 앞에'0' 을 붙이고 16진수는 리터럴 앞에 <mark>접두사 '0x' 또는 '0X' </mark>를 붙인다.

```css
int oct = 010;      //8진수 10, 10진수의 8
int hex = 0x10;     // 16진수의 10, 10진수로 16
```


JDK1.7부터는 중간에 <mark>구분자 '_'</mark>를 넣을 수 있게 되었다.

```css
long big = 100_000_000_000L;
long hex = 0xFFFF_FFFF_FFFF_FFFFL;
```


<mark> float 타입은 'f' </mark>를 붙이지 않으면 default double 타입이 된다. 
```css
float pi = 3.14f;     //접미사f 대신 F 사용가능 , 생략불가
double rate = 1.619d; //접미사d 대신 D 사용가능 , 생략가능
```

### 3. 문자 리터럴의 문자열 리터럴
```css
  char ch = 'J'; //문자 한 개 이상 저장할 수 없다.
  String name ="Java" //문자열을 저장


  String str =""; //ok, 초기화
  char ch = ''; //에러, 하나의 문자열을 넣어야한다.
  char ch = ' ';//ok, 공백으로 초기화
```
### 4. 문자열 결합
숫자 뿐만 아니라 아래와같이 두 문자열을 합칠 때도 덧셈(+)을 사용할 수 있다.
```css
  System.out.println(7 + " ");     //7
  System.out.println(" " + 7);     // 7
  System.out.println(7 + "");      //7
  System.out.println("" + "");     //
  System.out.println(7 + 7 + " "); //14
  System.out.println(" " + 7 + 7); //77

```
    
## 3. 기본형(Primitive Type) 종류와 크기

    기본형이란 논리형, 문자형,정수형,실수형 계산을 위한 실제 값을 저장하고 
    참조형은 객체의 주소를 저장한다. (기본형 외 나머지 타입들을 가리킴)

### 1. 기본형(Primitive Type) 종류
<table class="tg">
<thead>
  <tr>
    <th class="tg-1wig">종류\크기</th>
    <th class="tg-1wig">1byte</th>
    <th class="tg-1wig">2byte</th>
    <th class="tg-1wig">4byte</th>
    <th class="tg-1wig">8byte</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-baqh">논리형</td>
    <td class="tg-baqh">boolean</td>
    <td class="tg-baqh"></td>
    <td class="tg-baqh"></td>
    <td class="tg-baqh"></td>
  </tr>
  <tr>
    <td class="tg-baqh">문자형</td>
    <td class="tg-baqh"></td>
    <td class="tg-baqh">char</td>
    <td class="tg-baqh"></td>
    <td class="tg-baqh"></td>
  </tr>
  <tr>
    <td class="tg-baqh">정수형</td>
    <td class="tg-baqh">byte</td>
    <td class="tg-baqh">shout</td>
    <td class="tg-baqh">int</td>
    <td class="tg-baqh">long</td>
  </tr>
  <tr>
    <td class="tg-baqh">실수형</td>
    <td class="tg-baqh"></td>
    <td class="tg-baqh"></td>
    <td class="tg-baqh">float</td>
    <td class="tg-baqh">double</td>
  </tr>
</tbody>
</table>

> 논리형 - true와 false 중 하나를 값으로 가지고 조건식 논리적 계산에 사용

> 문자형 - char 문자를 저장하는데 사용, 변수 당 하나의 문자만 저장 가능

> 정수형 - 정수 값을 저장하는데 사용, 주로 int와 long이며 shout은 c언어와의 호환을 위해 추가(잘안쓰임)

> 실수형 - 실수 값을 저장하는데 사용, float, double이 있다.

### 2. 기본형(Primitive Type) 저장 범위

<table class="tg">
<thead>
  <tr>
    <th class="tg-baqh">자료형</th>
    <th class="tg-baqh">저장 가능한 값의 범위</th>
    <th class="tg-baqh">bit</th>
    <th class="tg-baqh">byte</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-baqh">Boolean</td>
    <td class="tg-0lax">false, true</td>
    <td class="tg-baqh">8</td>
    <td class="tg-baqh">1</td>
  </tr>
  <tr>
    <td class="tg-baqh">char</td>
    <td class="tg-0lax">0 ~ 35535 </td>
    <td class="tg-baqh">16</td>
    <td class="tg-baqh">2</td>
  </tr>
  <tr>
    <td class="tg-baqh">byte</td>
    <td class="tg-0lax">-128 ~ 127</td>
    <td class="tg-baqh">8</td>
    <td class="tg-baqh">1</td>
  </tr>
  <tr>
    <td class="tg-baqh">short</td>
    <td class="tg-0lax">-32768 ~ 32767</td>
    <td class="tg-baqh">16</td>
    <td class="tg-baqh">2</td>
  </tr>
  <tr>
    <td class="tg-baqh">int</td>
    <td class="tg-0lax">-2,147,483,648 ~ 2.147.483.647(20억)</td>
    <td class="tg-baqh">32</td>
    <td class="tg-baqh">4</td>
  </tr>
  <tr>
    <td class="tg-baqh">long</td>
    <td class="tg-0lax">-9.223.372.036.854.775.808 ~ 9223.372.036.854.775.807</td>
    <td class="tg-baqh">64</td>
    <td class="tg-baqh">8</td>
  </tr>
  <tr>
    <td class="tg-baqh">float</td>
    <td class="tg-0lax">1.4E-45 ~ 3.4E38</td>
    <td class="tg-baqh">32</td>
    <td class="tg-baqh">4</td>
  </tr>
  <tr>
    <td class="tg-baqh">double</td>
    <td class="tg-0lax">4.9E-324 ~ 1.8E308</td>
    <td class="tg-baqh">64</td>
    <td class="tg-baqh">8</td>
  </tr>
</tbody>
</table>


## 4. printf를 이용한 출력
printf()는 '지시자'를 통해 변수의 값을 여러 가지 형식으로 반환하여 출력하는 기능을 가지고 있다. 정수형 변수에 저장된 값을 10진 정수로 출력할 때는 지시자 '%d'를 사용한다.

```css
  System.out.println("age:%d", age); //age 변수명
  System.out.println("age:%d", 14);  //14 출력

```


자주 사용하는 지시자 표
<table class="tg">
<thead>
  <tr>
    <th class="tg-amwm">지시자</th>
    <th class="tg-amwm">설명</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-baqh">%d</td>
    <td class="tg-0lax">10진(<mark> d </mark>ecimal) 정수의 형식으로 출력</td>
  </tr>
  <tr>
    <td class="tg-baqh">%x</td>
    <td class="tg-0lax">16진(he<mark> x </mark>a -decimal) 정수의 형식으로 출력</td>
  </tr>
  <tr>
    <td class="tg-baqh">%f</td>
    <td class="tg-0lax">부동 소수점(<mark> f </mark>loating-point)의 형식으로 출력</td>
  </tr>
  <tr>
    <td class="tg-baqh">%c</td>
    <td class="tg-0lax">문자(<mark> c </mark>haracter)로 출력</td>
  </tr>
  <tr>
    <td class="tg-baqh">%s</td>
    <td class="tg-0lax">문자열(<mark> s </mark>tring)로 출력</td>
  </tr>
</tbody>
</table>

### 1. print 예제 
> println()의 단점 - 출력형식 지정불가
1. 실수의 자리수 조정불가 - 소수점 n자리만 출력하려면?
```css
System.out.println(10.0/3); //3.3333.. 
```
2. 10진수로만 출력된다. - 8진수,16진수로 출력하려면?
```css
System.out.println(10x1A) //26(10진수로 출력)
```
> printf()로 출력형식 지정가능 
1. 정수를 10진수,8진수, 16진수로 출력
```css
System.out.printf("%.2f", 10.0/3); //3.33(소수점 둘째자리까지 출력)
System.out.printf("%d", 10x1A); //26
System.out.printf("%x", 10x1A); //1A
System.out.printf("%s", Integer.toBinaryString(15)); //1111 2진수로 출력
```
2. 8진수와 16진수에 접두사 붙이지
```css
System.out.printf("%#0", 15) //017
System.out.printf("%#x", 15) //0xf
System.out.printf("%#X", 15) //0XF
```
3. 실수 출력을 위한 지시자 %f - 지수형식 (%e) ,간략한 형식($g))
```css
float f = 123.456789f;
System.out.printf("%f", f) //123.456787
System.out.printf("%e", f) //1.2345678e+02
```



###  2. printf()의 지시자
```css
System.out.printf("[%5d %n]", 10) //[   10] 공백3칸
System.out.printf("[%-5d %n]", 10) //[10   ] 공백 뒤에 3칸
System.out.printf("[%05d %n]", 10) //[00010] 빈자리를 '0'으로 채움
```
> %전체자릿수.소수점아래자릿f
```css
//전체 14자 중 소수점 아래 10자리
System.out.printf(d=%14.10f%n", d); //  1.02345678900
```
* 지정된 자릿수보다 큰 값을 넣게되면 값이 잘리지않고 저장 된 값을 모두 출력한다. 
* 소수점아래자릿수가 입력된 값보다 작으면 지정한만큼 잘려서 출력된다.단, 값은 그대로 저장이 되어있다.


## 3. Scanner
### Scanner 란?

    화면으로부터 데이터를 입력받는 기능을 제공하는 클래스

###  Scanner 사용방법

1. import 문 추가
```css
 impornt java.util.Scanner;
```
2. Scanner 객체 생성하기
```css
Scanner scanner = new Scanner(System.in);
```
3.  Scanner 객체 이용하기
```css
int num = scanner .nextInt();  //사용자에게 입력한 숫자를 저장

// 문자값을 숫자로 변경할때
String input = scanner.nextLine();  
int num = Integer.pareInt(input);
```

4. 정수형의 오버플로우

계수기를 예로 들어 4자리값이 최대인데 만약 "9999"에서 한번 더 누르면 "0000"이 되면서 오버플로우가 발생하는데
다시 1씩 증가한다.
  
9999+1  >  0000
최대값         최소값
0000-1   >  9999
최소값         최대값

 ![ch2_overflow.png](https://github.com/younme20/younme20.github.io/blob/master/assets/images/ch2_overflow.png?raw=true)

부호없는 정수 (4bit)의 경우 표현범위가 '0~15' 이므로 이 값이 계속 반복되고, 부호있는 정수(4bit)의 경우 표현범위가 '-8~7' 이브로 이 값이 무한히 반복된다. 

 ![ch2_ex2.JPG](https://github.com/younme20/younme20.github.io/blob/master/assets/images/ch2_ex2.JPG?raw=true)
