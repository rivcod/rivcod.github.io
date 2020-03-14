---
layout: post
title:  "C Programming - Ⅱ"
date:   2020-03-11 11:38:00 
lastmod: 2020-03-11 11:38:00
categories: [C, Programming, 혼자 공부하는 C언어]
sitemap:
  changefreq : daily
  priority : 1.0
---

## 2.1 상수와 변수


### 1.3.3 C 프로그램의 작성과 실행 예
1. Dev-C++ 컴파일러
2. Microsoft Visual Studio 컴파일러

## 1.4 C 프로그램의 구성

기본 구조는 도입부와 main() 함수, 그리고 호출함수 부분으로 구성된다.

[C 프로그램을 작성할 때의 일반적인 규칙]
+ C 프로그램은 반드시 하나 이상의 함수를 포함해야 한다.
+ main() 함수가 반드시 존재해야 한다.
+ 함수의 시작과 끝을 알리는 중괄호({})를 사용해야 한다.
+ 중괄호 안에는 변수 선언문, 치환문, 연산문, 함수 등의 명령을 기입한다.
+ 선행처리기(preprocessor)를 제외하고 문장의 끝에는 세미콜론(;)을 붙인다.

## 1.5 에러와 경고
`에러` : C 언어의 문법상 명백하게 잘못된 점이 있어 컴파일을 할 수 없는 경우 에러 메시지를 출력하고 컴파일을 거부한다.
`경고` : 코드의 내용이 의심스러워 보이기는 하지만 일단 컴파일이 가능한 경우 또는 이식성에 불리하거나 문법에서 권장하지 않는 방법으로 소스를 작성했을 때 발생한다.

<hr>


예제 1-2 : C프로그램의 구성요소를 알아보기 위한 프로그램
```c
/* 이 프로그램은 화씨를 섭씨로 변환하는 프로그램이다 */

#include <stdio.h>
// 변환 상수 정의
#define FZ_PT 32.0
#define S_FACTOR (5.0/9.0)

void main()
{
float fa, ce;
printf("Enter Fahrenheit temperature : ");
scanf("%f", &fa);
celsius=(fa-FZI_PT)*S_FACTOR;
printf("Celsius equivalent : %,1f\n", ce);
}
```




<div class="divider"></div>
