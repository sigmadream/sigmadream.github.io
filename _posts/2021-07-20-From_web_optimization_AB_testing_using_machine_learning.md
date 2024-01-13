---
layout: post
title: 머신러닝을 활용한 웹 최적화 A/B 테스트, 메타휴리스틱, 슬롯머신 알고리즘에서 베이즈 최적화까지
author: 이쓰카 슈헤이 (지은이), 김연수 (옮긴이)
tags: book
---

> 한빛미디어에서 제공받는 책으로 해당 리뷰를 작성하였습니다.

![책표지!]({{site.baseurl}}/images/20210725/01.jpg)

## 1

머신러닝, 딥러닝, 선형대수 그리고 통계처럼 AI 분야에서 직접적으로 사용되는 기술이나 이론은 어렵지 않지만, 막막하다. 개별적인 이론이나 기술을 학습하는 할 때, 좋은 교재도 많고 Coursera 등에 강의도 다양하기 때문에 생각보다 어렵지 않다(쉽다는 뜻은 아니다). 하지만 어느순간 막막함이 찾아온다. 당연하게도 학습자의 대부분이 풀고자 하는 문제는 `iris`처럼 단순하지 않고, `MNIST`처럼 쉽게 진행되지 않기 때문이다. 하지만 이런 사소한 질문보다 더 큰 의문이 앞을 가로막을 때가 있다.

> "도대체 이 기술을 어디에 써야 하는가?"

## 2.

사례를 찾아보고, 여기저기 풀지 못한 문제를 찾아가보지만 코끼리 다리를 만지는 것도 쉽지 않다. 대부분의 교재나 강의가 '모델'과 '해석' 기술을 가르치고 있기 때문이며, 실제 응용할 수 있는 사례를 찾기 위해선 적당한 분야(domain or field)가 있어야 되는데 어떤 분야에 내가 배운 AI 기술을 접목할 수 있을지 막막하다면, 이 교재로 시작해보자.

일단 이 교재는 "해보고(do), 배워보는(learn)" 형식의 책이다. 이런 종류의 책이 가지는 단점은 해보는 것이 중구난방(衆口難防)인 경우가 많고, 그게 아니라면 배우는 내용의 깊이가 전혀 없다는 점이다. 이 책은 이런 단점을 모두 피해간다. 이 책은 일관된 하나의 분야를 지향하고, 생각보다 깊이가 깊다. 그것도 많이 깊다. 그래서 난이도가 조금 올라가는 측면이 있지만 잘 작성된 코드를 제공하기 때문에 용기만 있다면 배우는데 큰 무리는 없다.

이 책의 제일 큰 혼돈은 제목인데, 왜냐하면 최적화라는 단어를 개발자가 접했을 때와 기획/마켓터가 받아들일 때 전혀 다른 상상을 할 것으로 예상되기 때문이다. 개발자는 이책을 AI 기술을 사용해서 웹 최적화를 진행할 듯 보이고, 기획/마켓터는 통계를 기반으로 UX를 개선할 것으로 받아들일 수 있다. 이 책은 그 모든 것을 다룬다. 기술적으로 웹을 최적화 하는 방법과 통계적으로 UX를 개선하는 방법을 모두 다룬다.

그래서 이 책은 개발자,마켓터, 기획자와 함꼐 보면 좋은 내용이 많다. 스타트업이나 팀단위 업무를 진행한다면 사내 스터디, 세미나, 기타 등등의 방법을 동원해서 관심있는 분야을 함께 읽어보길 권한다. 현재의 서비스를 개선해 볼 수 있다는 방법을 직접적으로 제공하기 때문이다.

![다양한 예제!]({{site.baseurl}}/images/20210725/03.jpg)

## 3

머신러닝, 딥러닝, 선형대수 그리고 통계를 실제 서비스 적용하는 사례가 흔하지 않다.A/B Testing를 시작으로 서비스에 적용본다면 현재 서비스에 대한 다양한 관점을 가져볼 수 있을 것이다. 개인적으로 가장 흥미롭게 봤던 예제는 샘플링을 사용해서 최적화된 색상을 찾는 방법이었다. 읽으면서 이 정도 수준의 예제는 당장 적용가능할 것으로 생각해서 친구들과 가벼운 토이 프로젝트를 진행하기로 했다.

> 파이썬으로 간단한 코드를 수행할 수 있고, 고등학교 수준의 통계적인 지식이 있다면 이 책의 예제를 시작으로 기술적인 도전을 시작해보자!

![이 정도의 예제!]({{site.baseurl}}/images/20210725/02.jpg)

## 4

필자는 이 책을 통해서 Toy 프로젝트를 진행하고 있다. Toy 프로젝트 진행하면서 도움이 된 다른 서적과 자료는 아래와 같다.

- [린 AI 사용자 유치, 그로스 마케팅, 성장 전략 수립에 인공지능 활용하기](https://www.aladin.co.kr/shop/wproduct.aspx?ItemId=272244605)
- [데이터 과학을 위한 통계](https://www.aladin.co.kr/shop/wproduct.aspx?ItemId=269943212)
  - [리뷰](https://sigmadream.github.io/practical_statistics_for_data_scientists/)
- [Reinforcement learning for the real world with Dr. John Langford and Rafah Hosn](https://www.microsoft.com/en-us/research/podcast/reinforcement-learning-for-the-real-world-with-dr-john-langford-and-rafah-hosn/)
- [A/B testing: A step-by-step guide in Python](https://medium.com/@RenatoFillinich/ab-testing-with-python-e5964dd66143)
- [A/B testing on app page changes](https://github.com/shanminlin/AB_test_analysis_app)