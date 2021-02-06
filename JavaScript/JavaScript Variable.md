## Variable(변수)
변경되거나 변경될 수 있는 것으로, 가변적이다. 

#### JavaScript 변수 기본문법
1. 문법은 한 줄에 하나씩 서술한다.
1. 문법이 끝나면 ;(세미콜론) 부호를 넣어준다.
1. 변수 시작에 let을 넣는다. (변수의 종류가 두 가지라 이를 구분하기 위해 사용한다.)
1. JavaScript는 위에서 아래로 순서대로 실행한다.

#### 변수가 적용되는 순서
1. 변수생성
1. 초기화
1. 사용

#### let, const, var?
>let : 새로운 값으로 바꿀 수 있다. 단, 변수 선언은 한 번만 가능하다.
```
let name = 'haha';
name = 'java';
console.log(name);
```
console.log 값은 java로 출력
```
java
```

>const : 상수(Constant)를 뜻하며, 안정적이다. 한 번 선언하면 변하지 않는다. 만약, 새로운 값으로 바꾸려고 하면 `TypeError:Arrignment to constant variable`가 발생한다. 기본적으로 사용하도록 한다.
```
const 하나 = 1;
하나 = 2; [x]
```

>var : 변수(Variable)을 뜻하며, 새로운 값으로 바꿀 수 있음을 뜻한다. 초반의 JavaScript는 var만 존재했고, 현재는 let, const 둘 중 하나로 선택해서 사용한다. 
<strong>변수 Hoisting현상과 예측하기 어려운 코드때문에, 가급적 사용하지 않는 것이 좋다.</strong>
```
var n = 1;
function test(){
  console.log(n);
  var n = 2;
  console.log(n);
}
test();
```
test()를 호출했을 경우, 아래와 같이 출력된다. 이는 변수 Hoisting 현상이 발생하기 때문이다.
```
undefined
2
```


## 변수 Hoisting
Hoisting이란 var를 사용하여 변수를 선언할 때, 해당 변수가 속한 범위(scope)를 최상단으로 올려버리는 현상을 말한다. 
<strong>여기서 말하는 범위(scope)란 block 레벨이 아닌 함수(function) 레벨을 뜻하며, 함수 내에서 선언된 변수는 함수 블록 내에서만 유효하고, 함수 외부에서는 유효하지 않는다는 것을 말한다.</strong> 
즉, 참조할 수 없다.
```
var n = 1;
function test(){
  var n; //hoisting -> n에 어떤 값도 할당되지 않은 상태로, undefined가 출력
  console.log(n);
  n = 2;
  console.log(n);
}
test();
```

## Data Type
#### 주석 
```
//한 줄로 주석을 달고 싶을 때 사용한다.
/*
  여러 줄 주석을 달고 싶을 때 사용한다.
*/
const number = 10;
```

#### String
Text String을 의미하며, 변수 선언 시에 " " 안에 값을 넣는다. 이모티콘, 숫자, 글자 등을 넣을 수 있으며 모두 텍스트로 인식한다.
```
const name = "namji";
const emotion = "🤦‍♂️";
```

#### Boolean
참과 거짓을 이진법으로 나타나며, true(0)/false(1)로 정의한다.
```
const what = true;
const what = false;
```

#### float
소수점 숫자(floating number)를 뜻한다.
```
const height = 163.2;
```

#### Number
정수(Integer)와 소수점 숫자를 모두 표현할 수 있다.