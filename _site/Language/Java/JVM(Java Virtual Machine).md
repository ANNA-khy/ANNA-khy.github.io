# JVM
* Java 어플리케이션은 JVM을 거친 뒤 OS를 거치기 때문에 OS에 독립적이다.
* 어플리케이션은 OS에 독립적이지만 JVM은 OS에 종속적이다.
* JVM을 사용하기 때문에 java로 만든 프로그램은 속도가 느리다.

# 메모리 구조
* method area: 클래스가 사용되면 클래스 파일을 읽어서 해당 영역에 저장한다.
* stack: method의 작업에 사용되는 공간으로 method가 작업을 마치면 해당 공간은 반납된다.
* heap: instance 변수가 생성되는 곳이다.
