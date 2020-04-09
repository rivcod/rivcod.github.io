---
layout: post
title:  "Database System #SQL"
date:   2020-03-12 11:38:00 
lastmod : 2020-03-12 11:38:00
categories: [knou, database]
sitemap :
  changefreq : daily
  priority : 1.0
---

## # SQL
  
### 1. 데이터베이스 언어

[SQL(Structured Query Language)]
1. 비절차적(선언형) 언어, 필요한 데이터만 기술
2. 인간의 언어와 유사하고 간단 명료함
<br>
<div class="divider"></div>

### 2. 데이터 정의 언어(DDL)
**명령어** : CREATE, ALTER, DROP
**객체** : TABLE, INDEX, VIEW, SCHEMA ...

> `스키마` = 데이터베이스
<br>
한 조직의 데이터베이스 시스템의 운영에 필요한 테이블, 인덱스, 뷰 등의 데이터베이스 객체의 집합

<div class="divider"></div>

### 3. 데이터 조작 언어(DML)
INSERT, UPDATE, DELETE, SELECT

[INSERT 문의 사용]
```
INSERT INTO 학과(단과대학, 학과이름, 졸업학점, 전화번호) VALUES ('자연과학대학', '농학과', 140, '02-1441-1361')
```

[UPDATE 문의 사용]
```
UPDATE 학과
  SET 주소 = 'http:// agri.knou.ac.kr'
  WHERE 학과이름 = '농학과'
```
```
UPDATE 학과
  SET 잔액 = 잔액 * 1.02
  WHERE 잔액 >= 500000
```

[DELETE 문의 사용]
```
DELETE FROM 테이블 이름
  WHERE 조건
```

**SAFE UPDATES 모드**
WHERE절이 없는 UPDATE/DELETE 문은 테이블의 전체 데이터를 변경/삭제할 수 있으므로
의도치 않은 데이터의 변경/삭제방지를 위해 MYSQL에서 지원하는 모드.
`!` 기본키가 아닌 컬럼을 대상으로 수정/삭제 조건을 명시할 경우 실행 여부를 결정

> 조건질의문
: 산술연산식, 함수 등을 사용하여 표현한 조건을 WHERE 절에 기술하여 조건을 만족하는 레코드만 검색하는 SELECT 문
(산술연산자, 비교연산자, 논리연산자)

[조건질의문의 사용]
```
SELECT 과목명, 학점, 선수과목 FROM 과목 WHERE 이수구분='전공필수'
```

> 데이터 정렬
1. ORDER BY 절을 사용
2. 검색 결과를 특정 컬럼에 대해 오름차순 또는 내림차순으로 정렬
(오름차순: ASC, 내림차순: DESC)

[데이터 정렬의 사용]
`? 학생의 계좌정보를 '잔액' 기준으로 각각 오름차순, 내림차순으로 정렬하라.`
```
SELECT * FROM 학생 RODER BY 잔액 ASC / DESC
```

> 특수연산자
: 범위 포함 여부, 부분 일치 여부, 포함 여부 등 관계형 데이터베이스에서만 사용되도록 고안된 연산자
(BETWEEN, LIKE, IN)

1. BETWEEN
```
SELECT 계좌번호, 잔액, 학생번호 FROM 계좌 WHERE 잔액 BETWEEN 200000 AND 400000
```

2. LIKE

3. IN



<div class="divider"></div>

### 4. 데이터 정의 언어

<div class="divider"></div>











