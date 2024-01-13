---
layout: post
title: 객체지향과 디자인 패턴
author: 최범균
tags: book
---

## 1
'객체지향'에 대한 엄밀한 정의와 원리적인 이야기를 읽을 수 있다. `SOLID`와 `DI`에 관련된 내용은 많은 도움이 되었다.

----

1. > 객체 지향 기법으로 작성된 프로그램은 객체들로 구성이 된다. 각 객체는 자신만의 데이터와 프로시저를 갖는다. 객체는 자신만의 기능을 제공하며, 각 개체들은 서로 연결되어 다른 객체가 제공하는 기능을 사용할 수 있게 된다. 객체는 다른 객체에 기능을 제공하기 위해 프로시저를 사용하는데, 이때 프로시저는 자신이 속한 객체의 데이터에만 접근할 수 있으며, 다른 객체에 속한 데이터에는 접근할 수 없다.

2. > 객체가 제공하는 모든 오퍼레이션 집합을 객체의 '인터페이스'라고 부르며, 서로 다른 인터페이스를 구분할 때 사용되는 명칭이 바로 타입이다. 여기서 말하는 인터페이스는 자바 언어나 C# 언어에 포함되어 있는 인터페이스가 아니라, 객체 지향에서 오퍼레이션 집합을 표현할 때 사용되는 용어이다. 인터페이스는 객체를 사용하기 위한 일종의 명세나 규칙이라고 생각하면 된다. [...] 실제 객체의 구현을 정의하는 것은 클래스(class)이다.

3. > 기능 실행을 요청하는 방식으로 코드를 작성하다 보면, 자연스럽게 해당 기능을 어떻게 구현했는지 여부가 감춰진다. 즉, 기능 구현이 캡슐화되는 것이다. 데미테르의 법칙(Law of Demeter) sms 'Tell, Don't Ask' 규칙을 따를 수 있도록 만들어 주는 또 다른 규칙이다. 데미테르의 법칙은 다음과 같이 간단한 규칙으로 구성된다.

4. > 상속은 한 타입을 그대로 사용하면서 구현을 추가할 수 있도록 해주는 방법을 제공한다.

5. > 다형성은 한 객체가 여러 가지 모습을 갖는다는 것을 의미한다. 여기서 모습이란 타입을 뜻하는데 즉, 다형성이란 한 객체가 여러 타입을 가질 수 있다는 것을 뜻한다.

6. > [...] 모두 상위 타입인 LogCollector 인터페이스에 정의된 기능을 실제로 구현하는데, 이들 클래스들은 실제 구현을 제공한다는 의미에서 '콘크리트 클래스'라고 부른다.

7. > [...] 인터페이스에 대고 프로그래밍하기 (program to interface) [...] 즉, 이 말은 실제 구현을 제공하는 콘크리트 클래스를 사용해서 프로그래밍하지 말고, 기능을 정의한 인터페이스를 사용해서 프로그래밍 하라는 뜻이다.

8. > 1.2 책임이란 변화에 대한 것 [...] 하지만 서로 다른 이유로 변경되는 것을 알아채려면 많은 프로그래밍 경험을 필요로 하기 때문에 경험이 적은 프로그래머가 단일 책임 원칙을 처으부터 잘 지키기란 쉽지 않다.

9. > instanceof와 같은 타입 확인 연산자가 사용된다면 해당 코드는 개발 폐쇄 원칙을 지키지 않을 가능성이 높다. 이런 경우에는 타입 캐스팅 후 실행하는 메서드가 변화 대상인지 확인해봐야 한다.

10. > 리스코프 치환 원칙은 기능의 명세(또는 계약)에 대한 내용이다. 

11. > 인터페이스 분리 원칙은 클라이언트 입장에서 인터페이스를 분리하라는 원칙이다.

12. > 고수준 모듈은 저수준 모듈의 구현에 의존해서는 안 된다. 저수준 모듈이 고수준 모듈에서 정의한 추상 타입에 의존해야 한다.

13. > [...] main() 메서드에서 생성자를 통해 이들이 사용할 객체를 주입(injection)한다는 점이다. 이렇게 누군가 외부에서 의존하는 객체를 넣어 주기 때문에, 이런 방식을 의존(dependency) 주입(injection)이라고 부르는 것이다.

14. > 이렇게 상위 클래스에서 실행 시점이 제어되고, 기본 구현을 제공하면서, 하위 클래스에서 알맞게 확장할 수 있는 메서드를 훅(hook) 메서드라고 부른다.
