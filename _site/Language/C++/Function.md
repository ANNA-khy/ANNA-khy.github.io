# Inline function
* 함수를 호출할 때 드는 오버헤드를 줄이고자 사용하는 방법으로 inline 키워드를 사용하며 함수를 호출하는 것이 아니라 함수 내용을 복사(inline화)한다.
<pre>
<code>inline double square(double a) { return a*a; }</code></pre>

# Functor
* 함수 개체(functinoal object)라고도 불리며 함수처럼 사용할 수 있는 클래스이다.
* 다음과 같이 functor를 정의한다.
<pre>
<code>class Nowage
{
public:
  nowage(int year) : year(year) {}
  int operator() (int x)
  {
    return year - x;
  }
private:
  int year;
};</code></pre>
* 다음과 같이 사용한다.
<pre>
<code>int main()
{
  Nowage now(2021);
  std::cout << now(1990) << std::endl;
}</code></pre>

# Lambda
* 함수가 간단한 함수일때 함수를 호출하는 대신 함수를 호출하는 곳에 inline시키는 표현식
* capture절 매개변수목록 { 람다 본문 }
* capture절에서 람다 외부의 변수들을 capture하여 접근할 수 있다.
* 매개변수목록은 생략가능하다.
* return type은 자동으로 추론된다.
<pre>
<code>[](int a) { return (a+1); }</code></pre>
