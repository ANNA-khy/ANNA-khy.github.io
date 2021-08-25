# Inline function
* 함수를 호출할 때 드는 오버헤드를 줄이고자 사용하는 방법으로 inline 키워드를 사용하며 함수를 호출하는 것이 아니라 함수 내용을 복사(inline화)한다.
<pre>
<code>inline double square(double a) { return a*a; }</code</pre>

# Lambda
* 함수가 간단한 함수일때 함수를 호출하는 대신 함수를 호출하는 곳에 inline시키는 표현식
