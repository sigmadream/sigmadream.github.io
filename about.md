---
layout: page
title: About
permalink: /about/
---

updated: 2023.07.21. - 2023년에 진행된 프리랜서 계약이 끝나고, 잠시 쉬는 동안 몇가지 업데트 하였음

### 관심분야

- 로그 수집, 분석 및 재현
  - `CQRS` 등과 같은 기술을 사용해서 로그를 수집, 관리 및 분석하는 것
- 데이터 수집 및 분석을 기반으로 한 서비스 설계, 구성 및 개발(구현)
  - 수집 및 분석 기술(`pandas`, `krangl`)을 활용해서 서비스 품질 및 성능 개선
  - 분석 결과를 대쉬보드를 만들어서 지표(혹은 KPI)를 기반으로 한 의사결정 과정 개선
  - 그 결과, 대부분의 업무가 [추천시스템](https://en.wikipedia.org/wiki/Recommender_system) 설계 및 구현을 중점적으로 진행하였음
- 함수형 프로그래밍([Functional programming](https://en.wikipedia.org/wiki/Functional_programming))
  - `Haskell`을 사용해서 데이터 구조와 알고리즘을 구현하는 것을 좋아함
    - 요즘은 Haskell로 데이터 분석하는걸 혼자서 연습해보고 있음, 실용적이지 않지만 Haskell을 다양하게 활용해보는 측면에서 긍정적으로 생각함
  - `Common Lisp`등을 활용해서 이런 저런 Toy 프로그램을 작성하는 것을 즐겨함
  - `Scala` 조금 할 수 있다는 이유로 [Apache Spark](https://spark.apache.org/)를 활용한 데이터 분석 서비스 팀에 강제로 차출되었던 경험이 있는데, 차출 경험은 별로였지만 서비스 개선 및 구현 경험은 재미있었음
- 컴파일러([Compiler](https://en.wikipedia.org/wiki/Compiler)) 구성
  - `LLVM`을 연구 중이며, DSL을 만들어서 잔잔한 유틸리티를 만들어서 사용하는 것을 즐겨함
  - `LLVM`은 현재 연구를 중단하였고, 현재는 [Online Judge](https://en.wikipedia.org/wiki/Competitive_programming)와 같은 코드 경진대회에 사용되는 채점 시스템 및 규칙을 활용해서 프로그래밍 언어 관련 학습 및 학습자 코드 검증 등을 주제로 연구를 계속해서 진행 중

### 사용하는 기술

- `Kotlin`과 `Java`(>= 17)

  - JDK는 17버전까진 학습했고, `Java Flight Recorder`를 사용해서 내가 운영하는 서비스를 프로파일링까지 했으나 서비스에 부하가 전혀 없어서(이것은 슬픈...일이지 않은가?!) 아쉽게도 별다른 성과는 없었음
  - `Spring`(>= 6.0) / `Spring Boot`(>= 3.0)
    - Kotlin을 사용해서 프로젝트를 진행 경험있으나 별로 유쾌하진 않았음
    - Spring의 경우 가능하면 Java를 활용하는게 아직은 안정적임
    - Jr. 개발자분들이 `Spring Boot`를 엄청 사용하셔서 덩달아 배웠음
    - `JUnit 5`로 확실히 정착 했음

- `C`(<=C99)/`C++`(>=17)

  - `C11`을 학습했지만, 2020년 작업했던 대부분의 펌웨어가 `C99`를 기반으로 작성해야 했다는 점에서 아쉬움
  - `C++17`를 사용해서 중급 규모의 프로젝트를 진행하면서 C++17을 기반으로 진행하였고, 코드 리뷰를 통해서 부족한 부분을 현재 보강하고 있음
  - 보강 중에 `C++22`까지 나와서 이젠 내가 뭘 학습해야 하는지 잊어버렸지만, `CMake`에 `C++20`을 설정하고 프로젝트 진행 중

- `Python`(>= 3.11)
  - Python 사용시 type hint를 사용하고 있었으나 다 부질없다 생각하고 지금은 `PyCharm`에서 제공하는 것 위주로 hint 작성, `Django`의 경우 문서를 참고해서 django 4.x에서 요구하는 형태로 코드를 변경하였고, 이젠 `pytest` 등을 활용해서 테스트 코드도 제법 작성할 수 있음
    - type hint가 생각보다 불편하고, 코드 가독성에 좋은 것 같지 않다는 느낌을 많이 받는 경우가 제법 많아서 아직은 어떻게 해야할지 보류 중
  - Django(>= 4.x), `FastAPI`(>= 0.100.0)
    - 새롭게 출시된 Django 버전을 계속해서 학습 중이며, 해당 프로젝트로 진행된 서비스가 1개(그것도 Django 2.x 시절) 뿐이라서 이제는 취미에 가까움
    - `Flask`보다 type hint 등에 강점을 보여서 `FastAPI`를 조금식 접해보고 있는데, 이것도 실제 서비스에 활용하는 수준이 아니라서 취미에 가까움

### 연락처

- Blog : [www.sangkon.com](http://www.sangkon.com)
- Mail : [sd](mailto:sigmadream@gmail.com)
