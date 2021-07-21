# mongoDB란?
mongoDB는 문서지향(Document-Oriented) 저장소를 제공하는 NoSQL 데이터베이스 시스템으로 제일 많이 사용한다. mongDB에서 데이터는 Document, 데이터의 집합을 Collection(RDMS=Table)한다. 스키마 제약 없이 자유롭고 BSON(Binary JSON) 형태로 각 문서가 저장되며 Array 나 Date 등 RDMS에서 지원하지 않던 형태로도 저장되기에 JOIN 필요 없이 문서를 좀 더 이해하기 쉬운 형태로 정보를 저장할 수 있다는 것이 특징이다. 객체 지향 프로그래밍과 잘 맞고 JSON을 사용할 때 아주 유용하기에 자바스크립트를 기반으로 하는 Node.js에서 가장 많이 사용되는 데이터베이스이다.

# NoSQL(Not Only SQL)이란?
RDMS와 SQL을 사용하는 않는 모든 데이터베이스 시스템 or 데이터 스토어를 일컬어 NoSQL이라고 한다. NoSQL은 빅데이터를 다룰 때 RDMS로만으로 트래픽을 감당하기 어려워져 이를 해결하기 위해 탄생되었다. 가장 큰 특징으로 확장성과 기용성, 높은 성능 그리고 다양한 데이터 형태를 수용할 수 있다는 것이다.

# BSON(Binary JSON)란?
Binary(2진법)로 인코딩(serialization) 된 JSON 문서를 말한다. 주로 JSON 형태의 데이터를 저장하거나 네트워크로 전송하는 용도로 사용된다.

# mongoDB 특징 정리
+ JOIN이 없으므로 JOIN이 필요 없도록 데이터 구조화가 필요하다.
+ 다양한 종류의 쿼리문(필터링, 수집, 정렬, 정규표현식 등)을 지원한다.
+ 스키마 없는(Schemaless) 데이터베이스를 이용한 신속한 개발이 가능하며 필드를 추가, 제거가 매우 쉬워진다.
+ 관리의 편의성
+ 쉬운 수평 확장성
+ 인덱싱 제공

# SQL과의 비교

#### 1. 용어 비교
|SQL 용어|mongoDB 용어|
|----|----|
|database|database|
|table|collection|
|index|index|
|row|JSON document|
|column|JSON field|
|join|embedding and linking|
|primary key|id field|
|group by| aggregation|

#### 2. 구문 비교
|SQL 구문(대소문자 구분 X)|mongoDB 구문(대소문자 구분 O)|
|----|----|
|CREATE TABLE USERS(a Number, b Number)|db.createCollection("user")|
|INSERT INTO USERS(3,5)|db.user.insert({a:3,b:5})|
|SELECT * FROM users|db.user.find()|
|SELECT a,b FROM users WHERE age=20|db.user.find({age:20},{a:1, b:1})|
|SELECT * FROM users WHERE age=20 ORDER BY name|db.user.find({age:20}.sort({name:1}))|

# mongoDB 설치 & 사용
+ https://relaxed-it-study.tistory.com/5

# mongoDB Documents

#### 1. Insert Documents
+ https://docs.mongodb.com/manual/reference/insert-methods/

#### 2. Update Documents
+ https://docs.mongodb.com/manual/tutorial/update-documents/

#### 3. Delete Documents
+ https://docs.mongodb.com/manual/tutorial/update-documents/

#### 4. Query Documents
+ https://docs.mongodb.com/manual/tutorial/query-documents/


