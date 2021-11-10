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
* NATURAL JOIN: 열의 이름이 같은 것만 JOIN
  * SELECT 열 FROM 테이블1 NATURAL JOIN 테이블2
* INNER JOIN: 일반적인 JOIN 연산
  * SELECT 열 FROM 테이블1 (INNER) JOIN 테이블2 ON 테이블1.열1 = 테이블2.열1
* OUTER JOIN: 한쪽 테이블에 일치하는 데이터가 없어도 null 값으로 출력
  * LEFT OUTER JOIN: 왼쪽 테이블의 데이터를 모두 출력
  * RIGHT OUTER JOIN: 오른쪽 테이블의 데이터를 모두 출력
  * FULL OUTER JOIN: 모든 테이블의 데이터를 모두 출력
  * SELECT 열 FROM 테이블1 LEFT(RIGHT) OUTER JOIN 테이블2 ON 테이블1.열1 = 테이블2.열1
* NATURAL/ON/USING
  * NATURAL JOIN: 열의 이름이 같은 것만 JOIN
    * SELECT 열 FROM 테이블1 NATURAL JOIN 테이블2
  * ON
    * SELECT 열 FROM 테이블1 JOIN 테이블2 ON 테이블1.열1 = 테이블2.열1
  * USING
    * SELECT 열 FROM 테이블1 JOIN 테이블2 USING 열1
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
## vIEW
* 가상 테이블을 만드는 것으로 특정한 사용자에게 실질적인 데이터베이스의 구조를 숨길 수 있다 => 보안
* CREATE VIEW 이름 AS <
