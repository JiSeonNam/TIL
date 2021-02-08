# 웹스토리지(Web Storage)
웹스토리지에는 로컬스토리지(Local Storage)와 세션스토리지(Session Storage)가 있다.
두 개의 스토리지는 모두 데이터를 브라우저에 저장하고, JavaScript API가 완전히 동일한 형태를 이룬다.
차이점은 데이터가 어떤 범위에서 얼마나 오래 보존되어있느냐의 차이뿐이다. 
세션스토리지는 웹페이지의 세션이 끝날 때 저장된 데이터가 지워지는 반면에, 로컬스토리지는 웹페이지의 세션이 끝나도 데이터가 지워지지 않는다.

### 세션스토리지(Session Storage)
브라우저의 창, 탭 마다 각각 저장되는 스토리지로 각 창이나 탭을 닫게 될 경우 저장된 데이터도 함께 소멸된다.
세션스토리지는 같은 웹페이지라도 창, 탭마다 각각 다르게 저장하므로 여러개의 데이터로 저장된다.

### 로컬스토리지(Local Storage)
브라우저의 창, 탭의 데이터가 서로 공유되며, 창이나 탭을 닫게 될 경우라도 브라우저에 데이터가 남아있다.
로컬스토리지의 데이터 영속성(Persistence)은 어디까지나 동일한 컴퓨터에서 동일한 브라우저를 사용할 경우에만 적용된다.
즉, 같은 컴퓨터에서 다른 브라우저를 사용하거나(크롬-IE-사파리를 쓴다던가) 다른 컴퓨터에서 같은 브라우저를 사용하는 경우
(집에서 크롬, 회사에서 크롬 사용)에는 서로 다른 스토리지에 데이터가 저장된다. 
서로 다른 기기나 브라우저 간에 데이터를 공유하고 영속하기 위해서는 클라우드(Cloud) 플랫폼 또는 데이터베이스(DB)에 저장돼야한다.
<br><br>


두 개의 스토리지 API는 완전히 동일하므로 사용방법은 로컬스토리지로 다루며, localStorage를 sessionStorage로 바꾸면 동일한 결과를 얻을 수 있다.
### 종류
#### 1. Session Storage
- 웹페이지 세션이 끝나면 데이터가 삭제된다.
- 창, 탭 간에 데이터가 공유되지 않으며, 각각의 세션으로 저장된다.

#### 2. Local Storage
- 웹페이지 세션이 끝나도 데이터가 남아있다.
- 창, 탭 간의 데이터가 공유되며, 창이나 탭을 닫아도 데이터가 남아있다.

### API 기본 사용법
웹스토리지는 기본적으로 키(key), 값(value)의 형식으로 이루어진 데이터로 저장된다.
window.localStorage/window.sessionStorage로 사용할 수 있으며, window를 생략한 localStorage/sessionStorage로 사용가능하다.

- 데이터 추가
```
//3가지 방법을 이용해 데이터를 추가할 수 있다.
localStorage.key값 = "value값";
localStorage["key값"] = "value값";
localStorage.setItem("key값", "value값");
```

- 데이터 읽기

```
//3가지 방법을 이용해 데이터를 읽을 수 있다.
localStorage.key값;
localStorage["key값"];
localStorage.getItem("key값");
```
![화면 캡처 2021-02-08 190623](https://user-images.githubusercontent.com/71870567/107205050-c164ec00-6a40-11eb-804f-9f64fbb92ee5.png)

- 데이터 삭제

```
localStorage.removeItem("key값"); 
```
![화면 캡처 2021-02-08 191113](https://user-images.githubusercontent.com/71870567/107205636-6ed7ff80-6a41-11eb-9e66-d3894b12f7f7.png)

- 모든데이터 삭제
```
localStorage.clear();
```

- 저장된 키/값 쌍의 개수
```
localStorage.length
```
![화면 캡처 2021-02-08 191835](https://user-images.githubusercontent.com/71870567/107206494-764bd880-6a42-11eb-99fb-63402a4217d7.png)


### 주의사항
웹스토리지는 오직 `String` 데이터 타입만 지원하므로, 숫자형 데이터를 저장할 경우 저장한 값이 아닌 이상한 값이 저장된다.

![화면 캡처 2021-02-08 192422](https://user-images.githubusercontent.com/71870567/107207138-49e48c00-6a43-11eb-86c4-870747ceb20e.png)

### JSON 형태로 데이터 추가/읽기
위와 같은 문제를 피하기 위해 데이터를 `JSON` 형태로 직렬화(serialization)하고, 읽은 데이터를 JSON 형태로 역직렬화(deserialization)하여 본래의 데이터를 얻는다.

![화면 캡처 2021-02-08 192741](https://user-images.githubusercontent.com/71870567/107207516-bbbcd580-6a43-11eb-8069-3b72c9e675ae.png)








