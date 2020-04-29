# Javascript
자바스크립트(JavaScript)는 객체(Object)기반의 웹의 동작을 구현할 수 있는 스크립트 언어이다.

특징
1. 객체 기반의 스크립트 언어.
2. 동적이며, 타입을 명시할 필요 없는 인터프리터 언어
3. 객체 지향형 프로그래밍, 함수형 프로그래밍을 모두 구현 가능
4. java와 같이 class 기반이 아니라 상속 개념이 없어 비슷한 개념의 prototype을 사용하여 정의
  *인터프리터 언어 : 컴파일 작업을 거치지 않고 소스 코드를 바로 실행할 수 있는 언어

객체란?
 - 자바스크립트에서 객체는 중요한 개념으로 이름과 값으로 구성된 프로퍼티의 정렬되지 않은 집합이다.
 ** 다른 변수에 값을 할당하거나 함수 인자로 넘길 때 값을 복사하여 전달하는 방식이 아니라 메모리 주소를 복사시키며 값 자체는 복사되지 않아 같은 객체를 참조하게 된다.
 
 1. 리터럴 표기를 이용한 객체의 생성 : {}를 사용하여 생성하며 ':'과 ,을 이용해 키 - 값 형태의 쌍으로 저장 후 접근자인 '.'을 이용하여 접근
  var me = {
   'name' : 'yeong snag',
   'birth' : 1994
  }
  me.name
 2. 생성자를 이용한 객체의 생성 : new 연산자를 사용하여 객체를 생성 및 초기화
  var day = new Date();
 
 3. Object.create() 메소드를 이용한 객체의 생성 : 지정된 프로토타입 객체와 프로퍼티를 가지고 새로운 객체를 생성
  --> 사용자가 프로토타입 객체를 직접 명시할 수 있다.
  --> javascript에서 사용하는 고전적인 상속 방법 중 하나
 
객체의 프로토타입

 
함수란?
 - function 키워드로 함수를 선언하며, 괄호 안에서 매개변수를 받아 return 을 통해 값을 반환하며 return 값이 없으면 기본값을 반환한다.
 
 함수의 선언
 1. 선언식
  대체로 우리가 자주 사용하는 함수 선언 방법중 하나이로 프로그래밍 언어에서의 함수 선언과 비슷한 형식이다.
  ex) function 함수명(){
   구현 로직
  }
 2. 표현식
  유연한 자바스크립트 언어의 특징을 활용한 선언 방식이다.
  ex) var 함수명 = function(){
   구현 로직
  };
 
- 선언식 vs 표현식
 함수 선언식은 호이스팅에 영향을 받고 함수 표현식은 호이스팅에 영향을 받지 않는다.
 예를 들어 함수 선언식은 코드를 구현한 위치에 상관없이 브라우저가 실행되면 호이스팅에 의해 맨 위로 끌어 올려진다.
 ** 호이스팅이란?
  - 함수 있는 선언들을 모두 끌어올려 해당 함수 유효 범위의 최상단에 선언
  - javascript var 변수 선언, 함수 선언문에 호이스팅 발생 --> let, const는 호이스팅이 발생하지 않는다.
  
- 함수 표현식의 장점
 호이스팅의 영향을 받지 않아 함수 선언식보다 유용하게 사용이 가능하다. 
  - 클로져로 사용
   ** 클로져는 함수를 실행하기 전에 해당 함수에 변수를 넘기고 싶을 때 사용.
  - 콜백으로 사용 
  
함수의 매개변수
 - parameter : 함수의 정의에서 전달받은 인수를 함수 내부로 전달하기 위해 사용하는 변수
   --> 함수를 호출할 때 인수로 전달되는 값에 대해 따로 타입 검사를 하지 않는다.
   --> 함수를 호출할 때 함수를 정의한 것보다 적은 인수가 들어와도 오류 발생을 시키지 않고 undefined 값으로 넘어온다.
   
 - arguments 객체 : 함수가 호출될 때 전달된 인수를 배열의 형태로 저장하며 arguments[0]과 같이 인수를 사용할 수 있다.
   ** arguments 객체는 배열과 비슷할 뿐 Array객체는 아니다.
   
 - default parameter : undefined 값으로 넘어오는 기본값은 원하는 값으로 설정할 수 있다.
   --> function add(a,b=1) : 인수가 하나만 전달될 경우 두번째 인수는 기본값으로 1이 들어간다.
   
 - rest parameter : 생략 접두사(...)를 사용하여 특정 위치의 인수부터 마지막 인수까지를 한 번에 저장
   --> arguments 객체와 같이 사용할 수 있다. restArgs[0],...
   

 

 
 
