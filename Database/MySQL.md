# MySQL 특징
# MySQL 명령어
## CREATE TABLE
* CREATE TABLE 테이블_이름 (</br>
  A1 D1, A2 D2, ..., An Dn,</br>
  (무결성제약))
* 무결성제약에는 primary key(Am), foregin key (Am) references r과같은 것이 있다.
## INSERT
* INSERT INTO 테이블이름 VALUES (....)
## DELETE
* DELETE FROM 테이블이름 WHERE ...
## UPDATE
* UPDATE 테이블이름 SET 업데이트내용 WHERE 조건
## SELECT
* FROM 절에 테이블이 여러개이면 cartesian곱
* WHERE 컬럼 LIKE '%규칙%'
* ORDER BY ASC/DESC
## JOIN
* INNER JOIN: 일반적인 JOIN 연산
  * SELECT 열 FROM 테이블1 INNER JOIN 테이블2 ON 테이블1.열1 = 테이블2.열1
* OUTER JOIN: 한쪽 테이블에 일치하는 데이터가 없어도 null 값으로 출력
  * LEFT OUTER JOIN: 왼쪽 테이블의 데이터를 모두 출력
  * RIGHT OUTER JOIN: 오른쪽 테이블의 데이터를 모두 출력
  * SELECT 열 FROM 테이블1 LEFT(RIGHT) OUTER JOIN 테이블2 ON 테이블1.열1 = 테이블2.열1
* IN/OUTER는 생략 가능
## SET
* UNION: 합집합
* INTERSECT: 교집합
* EXCEPT: 차집합
## Aggregate fucntions
* AVG
* MIN/MAX
* SUM
* COUNT
## CASE
* CASE WHEN 조건 THEN 반환값 ELSE 반환값 END AS 별칭
## Clause
* some
* all
* exists
* with
