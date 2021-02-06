아래는 Nomad Coders의 '[바닐라 JS로 크롬 앱 만들기](https://nomadcoders.co/javascript-for-beginners/lobby)' 강의를 듣고 정리한 내용이다. 
<br>

# 왜 JavaScript인가?
### 웹에 쓰이는 유일한 프로그래밍 언어이다. 
- 프론트엔드 일을 하고 싶다면, 선택할 수 있는 언어는 오직 JavaScript가 유일하다.
- 백엔드 일을 하고 싶다면, Python, Ruby, Java, Haskell 등의 언어를 사용할 수 있다.

웹 사이트를 interactive하게 만들고 싶을 때, JavaScript를 사용할 수 있다.
- 장점 : 분열(fragmentation)이 없다. 즉, 모두 같은 언어로 얘기할 수 있다.
- 단점 : 업데이트를 마음대로 할 수 없거나, 할 수 없는게 존재한다. 

그러나 웹은 빠르게 발전하고 있고, JavaScript가 웹에서 쓰일 수 있는 유일한 언어이기 때문에 JavaScript도 그에 맞춰 빠르게 발전하고 있다. JavaScript를 능수능란하게 사용할 수 있는 개발자는 없다.

### JavaScript를 이용해 만들 수 있는것이 무엇인가?
- 할 일 목록 저장
- 위치 저장
- Real Time(실시간)을 이용한 애플리케이션
- 데스크톱 애플리케이션(예. vsc, atom)
- 앱어플리케이션
- 비디오게임
- 3D 라이브러리

### 프론트엔드에서 왜 JavsScript를 사용하는가?
- 만들고 다른 언어로 교체하지 않았다.
- 모든 컴퓨터에는 기본적으로 브라우저를 사용하고 있고, 브라우저는 JavaScript로 돌아간다. 즉, 모든 컴퓨터에서 JavaScript를 사용할 수 있다. 이는 모든 컴퓨터가 이 언어를 이해한다는 것을 뜻한다.
- 위는 별도의 행위를 하지 않아도 JavaScript를 사용할 수 있다는 것을 뜻한다.
<br>

# JavaScript 버전
JavsScript는 언어이고, ECMAScript는 Specification을 의미한다. JavaScript의 Specification에 대한 업데이트가 이루어지면서 버전이 존재한다. [[더 알아보기]](https://developer.mozilla.org/ko/docs/Web/JavaScript/%EC%96%B8%EC%96%B4_%EB%A6%AC%EC%86%8C%EC%8A%A4)
- ES5 = ECMAScript5 = Specification 5버전
- ES6 = ECMAScript6 = Specification 6버전

JavaScript는 중앙집중화(Centralization)이 되어있어, 누군가 업데이트를 할 경우 모든 브라우저에 적용된다. 모든 브라우저는 이 Specification을 받아 각자의 방식으로 실행하여 같은 결과를 이루려고 한다. (브라우저마다 다른 버전의 ES를 지원한다.) 
ES5, ES6보다 일반적인 JavaScript가 중요하기에 이것에 대해 먼저 배울 것이다.
<br><br>



# Vanilla JS
Vanilla는 JavaScript의 한 종류로, 브라우저를 통해 제공된 JavaScript를 의미한다. Libarary와 Framework가 전혀없는 JavaScript를 의미한다.

### Vanilla JS를 배워야 하는 이유
Vanilla JS 정말 못생겼다. 하지만, 그걸 모두 바꾸려면 엑박천지가 뜰 것이다. 새로운 것으로 대체할 수 있는 것이 아닌 핵심을 배우기 위해서는 Vanilla JS를 배워야 한다. 이유는? JavaScript에 재능있는 사람을 찾을 수 없기 때문이다. React나 jQuery를 아는 사람은 찾기 쉽고, Library, Framework를 아는 사람은 찾기 쉽다.

예를 들어, 포토샵을 잘 다루지만, 색감에 센스가 없거나, 색의 구성도 모르고 멋진 사진이 뭔지 감각이 없는 사람처럼 JavaScript를 제대로 모르고 사용한다는 건 있어서는 안된다.
![화면 캡처 2021-02-06 000510](https://user-images.githubusercontent.com/71870567/107051338-b0816400-680f-11eb-8e84-7d9bb4e23c74.png)

위 사진은 Vanilla JS코드의 기본 문법과 처리하는 속도를 나타낸다. 120만개가 넘는 Operation을 1초에 수행할 수 있다. Vanilla JS를 배운다는 것은 웹에서의 기초가 되는 언어를 배우는 것이다.




