# MySQL 특징
# MySQL 명령어
## JOIN
* INNER JOIN: 일반적인 JOIN 연산
  * SELECT 열 FROM 테이블1 INNER JOIN 테이블2 ON 테이블1.열1 = 테이블2.열1
* OUTER JOIN: 한쪽 테이블에 일치하는 데이터가 없어도 null 값으로 출력
  * LEFT OUTER JOIN: 왼쪽 테이블의 데이터를 모두 출력
  * RIGHT OUTER JOIN: 오른쪽 테이블의 데이터를 모두 출력
  * SELECT 열 FROM 테이블1 LEFT(RIGHT) OUTER JOIN 테이블2 ON 테이블1.열1 = 테이블2.열1
* IN/OUTER는 생략 가능
## CASE
* CASE WHEN 조건 THEN 반환값 ELSE 반환값 END AS 별칭
