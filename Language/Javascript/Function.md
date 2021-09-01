# Function
* 웹브라우저는 선언적 함수부터 읽는다.
* 외부 함수 안에 내부 함수를 사용하여 함수끼리 충돌(이름)을 막는다.

# Callback function
* 매개변수로 전달하는 함수는 callback 함수라고 한다.
<pre>
<code>function calculator(callback, x, y){
      return callback(x, y);
}
calculator(function(x, y){ return x+y; }, 1, 2);</code></pre>

# Closure
* 지역변수가 외부에 남아 계속 사용할 수 있다. 

# Prototype
* 객체를 생성할 때 메소드가 겹치면 메모리 공간의 낭비가 일어난다.
* 생성자 함수로 생성된 객체가 공통적으로 가지는 공간을 prototype이라고 한다.
<pre>
<code>function Person(...){
      ...
      }
      Person.prototype.함수명 = function () {};</code></pre>
      
