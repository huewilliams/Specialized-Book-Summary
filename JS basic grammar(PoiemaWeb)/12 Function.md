# Fuction 함수
## 함수는 일급 객체이다.
함수는 객체(`일급 객체`, First-class object)이다. 따라서 다른 값들처럼 사용할 수 있다. 즉, 변수나 객체, 배열 등에 저장할 수 있고 다른 함수에 전달되는 인수로도 사용할 수 있으며 함수의 반환값이 될 수도 있다. 무명의 리터럴로 표현 가능하다.

### First-class object (일급 객체)
 프로그래밍 언어의 기본적 조작을 제한없이 사용할 수 있는 대상. 다음 조건을 만족시 일급객체로 간주
- 무명의 리터럴로 표현이 가능하다.
- 변수나 자료 구조(객체, 배열 등)에 저장할 수 있다.
- 함수의 매개변수에 전달할 수 있다.
- 반환값으로 사용할 수 있다.

## 함수의 선언
### 함수 표현식 
함수 리터럴 방식으로 함수를 정의하고 변수에 할당 가능. 함수 호출 시 함수명이 아닌 할당된 변수명으로 사용해야 함.

### 익명 함수(anonymous function)
함수 표현식에서는 함수명을 생략할 수 있다.

## 생성자 함수
### Function 생성자 함수
new Function(arg1, arg2, ... argN, functionBody) , 함수 리터럴 방식도 결국 내장 Function 생성자 함수의 생성의 축약법(short-hand) 이다.

## 함수 호이스팅 
JS 는 모든 선언을 호이스팅(Hoisting)한다. 따라서 함수가 선언되기 전에 호출이 가능하다.
- 선언문 정의 함수 : 함수 선언, 초기화, 할당이 한번에 이루어짐(호이스팅 될때)
- 함수 표현식 : 변수 호이스팅 발생( 변수 초기화 후 할당 문에서 할당)
=> 함수 표현식을 사용하는 것이 프로그래밍 구조적으로 좋음

## 매개변수 전달
인자(parameter) vs 인수(argument)

### Call-by-value 
원시 타입 매개변수는 전달 시 값이 복사되어 전달된다.

### Call-by-reference 
참조형 매개변수는 객체의 참조값이 전달된다.

## 함수 복수값 반환
return [area, volume];

### 함수 객체의 프로퍼티
함수는 객체이므로 프로퍼티를 가질 수 있다.

### arguments
함수 내부에서만 사용가능한 객체이다. 함수의 매개변수들을 담아 순회가능하다. arguments 는 매개변수의 수가 정해지지 않은 가변 인자 함수를 구현할 때 유용하다. arguments 는 유사 배열 객체이므로 length 이외의 배열 메소드를 사용할 경우 에러가 난다. 배열 메소드를 사용하려면 Function.prototype.call, Function.prototype.apply 를 사용해야 한다.

## 함수 프로퍼티

### caller 프로퍼티
자신을 호출한 함수를 의미한다.

### length 프로퍼티
함수 정의 시 작성된 매개변수 갯수를 의미한다.

### name 프로퍼티
함수명을 나타낸다. 기명함수의 경우 함수명을 값으로 갖고 익명함수의 경우 빈문자열을 값으로 갖는다.

### prototype 프로퍼티
함수가 객체를 생성하는 생성자 함수로 사용될 때, 생성자 함수가 생성한 인스턴스의 프로토타입 객체를 가리킨다.

## 함수의 종류

### 즉시 실행 함수(IIFE, Immediately Invoke Function Expression)
함수의 정의와 동시에 실행되는 함수이며 최초 한번만 호출되며 다시 호출할 수는 없다. 초기화 처리에 이용된다. 형태 : (function(){}()); JS엔진이 {}블럭문 끝에 자동으로 세미콜론(;)을 추가하므로 ()로 묶어준다.

### 내부 함수(Inner function)
함수 내부에 정의된 함수를 내부 함수라 한다.
내부 함수는 자신을 포함하고 있는 부모 함수의 변수에 접근할 수 있다. 하지만 부모 함수는 자식 함수(내부 함수)의 변수에 접근할 수 없다. 또한 내부함수는 부모함수의 외부에서 접근할 수 없다.

### 재귀 함수(Recusive function)
자기 자신을 호출하는 함수를 말한다. 탈출 조건을 만들지 않으면, 함수가 무한 호출되어 stack overflow 에러가 발생한다.

### 콜백 함수(Callback function)
함수를 명시적으로 호출하는 방식이 아니라 특정 이벤트가 발생했을 때 시스템에 의해 호출되는 함수를 말한다. 대표적으로 이벤트 핸들러에 사용한다. 콜백 함수는 매개변수를 통해 전달되고 전달받은 함수의 내부에서 어느 특정시점에 실행된다. 또한 콜백 함수는 주로 비동기식 처리 모델에 사용된다.