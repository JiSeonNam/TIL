# 자바 언어
Java 프로그래밍 언어에서 모든 소스 코드(Source code)는 .java 으로 끝나는 일반 텍스트 파일로 저장된다. .java 파일은 1차적으로 javac(자바시) 컴파일러에 의해 ByteCode인 .class 파일로 컴파일된다. 이후, 2차적으로 JVM(Java Virtual Machine)에 의해 운영체제에 작용하는 기계어로 컴파일되어 Java 프로그램이 실행된다. JVM 때문에 .class 파일은 어느 운영체제에서 사용이 가능하다. 
ByteCode란 사용자가 작성한 .java 소스코드파일을 JVM이 운영체제에 실행가능한 명령어 집합파일로 컴파일하는 과정 중에 필요한 코드를 의미한다. 

![getStarted-compiler](https://user-images.githubusercontent.com/71870567/108070845-55216280-70a8-11eb-88a9-6fcfd9b7f24a.gif)

![helloWorld](https://user-images.githubusercontent.com/71870567/108070886-64081500-70a8-11eb-8143-e808a91bfcc7.gif)
<br><br>

# 자바 플랫폼
플랫폼은 프로그램이 실행되는 하드웨어 또는 소프트웨어 환경을 의미한다. 일반적인 플랫폼은 하드웨어 기반 위에서 실행되는 소프트웨어 기반 플랫폼 인 것과 달리 자바 플랫폼은 이와는 달리 두 가지 구성요소가 있다.

- JVM(Java Virtual Machine) : 자바에서 명령을 실행하는 일련의 소프트웨어 프로그램으로 일반적으로 Java ByteCode로 작성된다. 일반적인 애플리케이션은 OS(운영체제)와 직접적으로 연관되어 전달되는데 비해, Java는 JVM을 거쳐서 컴파일되기 때문에 운영체제에 상관없이 사용할 수 있다.
- API(Java Application Programming Interface)

여기서 API는 유용한 기능을 제공하는 소프트웨어 구성요소의 대규모 컬렉션이라고 볼 수 있다. 이는 class와 interface 라이브러리로 그룹화되어있다. 

![getStarted-jvm](https://user-images.githubusercontent.com/71870567/108071036-91ed5980-70a8-11eb-9c00-a7d799402408.gif)
<br><br>

# 객체(Object)
현실세계에서 상태(state)와 행동(behavior)에 빗대어 생각해 볼 수 있다. 객체는 필드(field)에 상태를 저장하고, 메소드(method)에 행동을 노출한다. 
메소드는 객체 내부에서 객체와 객체간의 주요 커뮤니케이션 역할을 한다.

![concepts-object](https://user-images.githubusercontent.com/71870567/108071569-3a032280-70a9-11eb-8aad-c1339f1fa110.gif)

개별 소프트웨어 객체에 코드를 번들링하면 여러가지 이점을 얻을 수 있다.
1. Modularity(모듈리티) : 객체 소스코드는 다른 객체 소스코드와 독립적으로 작성 및 유지될 수 있다. 일단 생성하면, 객체는 시스템 내부를 쉽게 통과할 수 있다.
2. Information-hiding(정보숨기기) : 객체의 메소드로만 상호작용하게 되므로, 바깥에서 내부 구현 세부사항을 숨길 수 있다.
3. Code re-use(코드 재사용) : 만약 이미 존재하는 객체가 있다면 사용할 수 있다. 이를 통해 복잡한 작업별 개체를 구현, 테스트, 디버그 할 수 있으며, 자신의 코드로 실행할 수 있따.
4. Pluggability and debugging ease(플러그 가능성 및 디버깅 용이성) : 만약 특정 객체가 문제가 있는 것으로 판단된다면, 해당 객체를 제거하고 다른 객체로 교체할 때 플러그를 꽂을 수 있다. 이것은 현실세계와 비슷하게 볼트가 부러질 경우 전체 기계를 고치는 것이 아니라 볼트를 교체하는 것과 같다.
<br><br>

# 클래스(Class)
객체지향적인 관점에서, 클래스는 개별 객체가 생성되는 청사진(blueprint)을 의미한다. 
즉, 서로 관련된 변수들을 정의하고 이들에 대한 작업을 수행하는 메소드를 함께 정의한 것을 클래스라 일컫는다.
<br><br>
