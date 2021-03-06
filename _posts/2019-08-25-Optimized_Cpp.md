---
layout: post
title: C++ 최적화 
author: 커트 건서로스 (지은이), 옥찬호 (옮긴이)
tags: book
---

## 1

이번 파이콘(2019)에서 [파이썬 3.7 어찌 그렇게 빨라졌나](https://www.pycon.kr/program/talk-detail?id=127)세션을 들었다. 해당 세션을 들으면서 `CPython`에 대한 호기심이 생겼고, 덕분에 C/C++을 좀 더 공부해야겠다고 생각했다. 약 10년 가까이 Java와 Python으로 대부분의 업무를 처리했는데, 아주 어린시절 정말 즐겁게 가지고 놀던 언어인 C/C++에 대한 아련함이 떠올랐지만 너무 오랜 시간 해당 언어를 사용하지 않아서 코드 작성, 개발 환경, 그리고 용례나 관례에 대한 감이 전혀 없는 상태였다.

![이것이 책 표지]({{site.baseurl}}/images/20190825/01.jpg)

## 2

C++ 문법은 예전에 배워서 대충 알고 있다고 생각해서, 문법도 복습하고 요즘 나오는 C++ 용례나 관례를 알아보고 싶었는데, 책에서 C++11, C++14, 그리고 C++17 이런거 보면서 약간 동공지진(!)이 왔다.

![C++ 17]({{site.baseurl}}/images/20190825/02.jpg)

대부분의 내용은 일반적인 C++(책을 찬찬히 읽어본 결과 C++11이전?)에 대한 내용은 기본적으로 알아야 읽을 수 있다. 제목에서 <<최적화>>라고 해서 약간 어렵겠진 생각했는데 C++에 대한 문법 이해와 일반적인 코드 작성 능력만 있으면 읽는데는 크게 무리없을 것으로 생각된다. 앞부분에 개략적인 내용이 나오니 그 부분부터 잘 읽어두면 좋을 듯 싶다. 그리고 <<검색 및 정렬 최적화>>와 <<자료구조 최적화>> 부분등과 같이 여러 언어에서 사용하는 기법의 경우 C++ 뿐만 아니라 Java나 Python 등에서 고려해볼만한 내용이 많았다. 

## 3

C++11 이후로 문법에 몇가지 변화가 있었고, 문법뿐만 아니라 개념적으로 변화가 있었던 것으로 보인다. 해당 책에선 C++11 이후의 문법뿐만 아니라 C++11 이전의 경험을 가진 개발자를 위해서 두 가지 설명을 병행해서 하기 때문에 C++ 문법을 아는 개발자라면 코드 리딩 및 작성에서 좋은 지침이 될 것이다.

![어색한 맞춤법]({{site.baseurl}}/images/20190825/03.jpg)

번역자분의 C++에 대한 탁월한 식견, 그리고 좋은 번역 덕분에 약간 어렵지만 많은 도움이 되는 책을 읽었다. 덕분에 CPython을 분석하는데 여러가지 도움이 되었다.
