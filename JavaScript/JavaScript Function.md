아래는 Nomad Coders의 '[바닐라 JS로 크롬 앱 만들기](https://nomadcoders.co/javascript-for-beginners/lobby)' 강의를 듣고 정리한 내용이다. 

# Function
함수(function)는 어떤 것의 기능으로, 어떤 걸 수행하려는 한 부분을 의미한다. 브라우저에 내장되어 있는 JavaScript는 Object에 넣어서 사용할 수 있다. console.log, alert 등은 내장함수(built-in function)를 뜻하며, Object이다.


- 사용방법 : function 함수명(){}
```
console.log(console); //console은 Object이며, log는 console Object 안에 있는 함수를 의미한다.
t {
  log: [Function],
  error: [Function],
  info: [Function],
  warn: [Function],
  dir: [Function],
  time: [Function],
  timeEnd: [Function],
trace: [Function],
  assert: [Function],
  clear: [Function],
  stdout: { [Function] clear: [Function] },
 _times: {} ...
}
```

### 인자(arguments)
인자란 어떤 함수로 전달되는 인자들의 값을 가지고 있는 배열과 유사한 형태의 객체를 의미한다. 인자를 통해 함수에게 외부에 있는 데이터를 줄 수 있다.

```
function sayHello(name, age){
  console.log('hello',name," you have ",age,years of age.);
}
sayHello("namejiseon", 34); //hello namjiseion you have 34 years of age.
```

### 백틱(``)
JavaScript에서 "", ''은 둘 다 String을 의미한다. "(쌍따옴표)로 시작하면 "로 끝내고, '(따옴표)로 시작하면 '로 끝낸다. 백틱은 새로운 String 방식으로, 함수를 호출할 때 사용한다.
```
function sayHello(name, age){
  console.log(`hello ${name} you are ${age} years old.`);
} 
sayHello("namjiseon", 34); //hello namjiseon you are 34 years old.
```

### return
함수의 반환값을 얻고자 할 때 사용한다. 즉, 어떤 함수의 결과를 return을 통해 반환하여 다른 곳으로 넘겨주거나, 해당 함수를 중지시키고자 할 때 사용한다. <strong>return이 없이는 함수의 반환값을 외부로 보낼 수 없다.</strong>

- 역할
1. 값을 반환하는데 사용한다.
1. 지역변수를 알고자 할 때 사용한다.
1. 현재 진행중인 함수를 중지할 때 사용한다.

예) 반환값이 없을 경우
```
function book(name, color){
    console.log(`${name}, ${color}`); //JohnSnow, white
}
const bookInfo = book("JohnSnow", "white"); //bookInfo = book 함수의 반환값을 의미한다. 
console.log(bookInfo); //undefined, book 함수의 반환값이 없기 때문에 undefined가 출력된다.
```

예) 반환값이 있을 경우
```
const calculator = {
  plus: function(num1, num2){ //더하기
    return num1 + num2;
  },
  minus: function(num1, num2){ //빼기
    return num1 - num2;
  },
  multiple: function(num1, num2){ //곱하기
    return num1 * num2;
  },
  divide: function(num1, num2){ //나누기 몫
    return num1 / num2;
  },
  reminder: function(num1, num2){ //나누기 나머지
    return num1 % num2;
  }
}

const plus = calculator.plus(5, 5);
const minus = calculator.minus(5, 5);
const multiple = calculator.multiple(5, 5);
const divide = calculator.divide(5, 5);
const reminder = calculator.reminder(5, 5);
console.log(plus); //10
console.log(minus); //0
console.log(multiple); //25
console.log(divide); //1
console.log(reminder); //0
```

예) 진행중인 함수를 중지하고자 할 때
진행중인 함수를 중단하고 나오고 싶을 때 사용하며, 변수가 필요할 경우 return을 쓰고 해당 값이 필요없다면 return false 또는 return 만 작성한다.
```
const test = function(){
  const x = 1;
  const y = 10;
  if(x == 1){
    return y; //x의 값이 1일 경우 y값을 반환한다.
  }
  y = x + 1;
  ...중략
}

console.log(test); //10 
```  
<br>

# JS DOM Functions
HTML이 JavaScript와 함께 쓰려고 하면 어떻게 동작하는지 알아보자. 아래는 console.log(document)의 로그를 출력한 모습이다.
document도 Object임을 알 수 있으며, document를 대표하는 HTML을 보여준다.

![화면 캡처 2021-02-06 233052](https://user-images.githubusercontent.com/71870567/107121002-6a8dd400-68d3-11eb-8573-996a8721f41b.png)

JavaScript는 HTML에 있는 모든 요소를 가지고 와서 Object로 만든다. 따라서 모든 HTML은 Object가 될 수 있다. 
모든 Object의 함수를 DOM(Document Object Module) 형태로 변경할 수 있다.


```
<h1 id="title">이것은 타이틀</h1>
<script>
  const title = document.getElementById("title"); 
  title.innerHTML = "change the title"; //title 내용을 바꾼다.
  title.style.color = "red"; //title의 컬러를 바꾼다.
</script>
```

### console.dir
DOM 객체의 메서드를 보고 싶을 경우 사용한다. 
```
console.dir(title); 
```
![화면 캡처 2021-02-06 234642](https://user-images.githubusercontent.com/71870567/107121410-97db8180-68d5-11eb-9f7f-c4551f6783b5.png)









