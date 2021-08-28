## 함수 템플릿(function template)
함수의 정의된 형태는 같지만 타입만 다를 때 template을 사용하여 정의한다.
<pre>
<code>template &#60typename T&#62
T 함수명(T a, T b)
{
...
}
</code></pre>

## 클래스 템플릿(class template)
함수 템플릿과 마찬가지로 타입에 따라 클래스를 생성할 수 있다. 생성할 때는 타입을 정확히 명시해주어야 한다.
<pre>
<code>template &#60class T, class Allocator = allocator&#60T&#62&#62
class vector;

...

vector&#60int&#62 arr;
</code></pre>
* T는 element의 타입이다.
* Allocator는 메모리 안에 요소들의 저장공간을 release/require 하는 데 사용한다.
