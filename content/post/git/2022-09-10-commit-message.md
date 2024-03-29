---
title: "깃 커밋 메시지 작성 방법"
date: 2022-09-10T16:00:00+09:00
tags: ["Git", "협업"]
---

## 커밋 메시지란?

말 그대로 깃 커밋을 할 때 남기는 메시지.
나는 깃을 이용할 때에 CLI보단 Git Fork나 SourceTree같은 GUI툴을 사용하는 편이다.

프로젝트를 진행하거나 실무를 진행할 때에도 혼자서만 작업을 진행하다보면 커밋 메시지를 딱히 신경쓰지 않게 되더라.

그렇게 업무를 진행하다보면 이 부분에 대해서 의문이 생기고 뭔가 룰이 필요하다고 느끼는 순간이 온다.

## 커밋 메시지가 필요하다고 생각한 이유

커밋 메시지를 마음대로 남기다 보면 분명 이 메시지에 규칙이 필요하다고 느끼는 순간이 오게된다.

내가 느낀 지점은 크게 3가지가 작용했다.

1. 업무, 프로젝트를 진행하다가 과거 코드를 분석하고 싶을 때
2. 팀원 또는 내가 잘못 푸시하거나 배포한 코드를 확인하고 싶을 때
3. 개발 코드 및 운영 코드를 롤백하고 싶을 때

이런 경우에 커밋 메시지의 규칙이 있었으면 좋겠다고 생각했다.
해당 커밋에 태그를 잘 남겨놓았으면 모를까, 어찌어찌 문제가 있거나 보고싶은 커밋을 찾았더라도
메시지가 잘 남겨져있지 않으면 일일히 코드를 확인해야 함을 느꼈다.

커밋 메시지를 잘 작성해 뒀더라면, 빠르게 내용을 파악할 수 있지 않을까?

## 커밋 메시지 레퍼런스 찾아보기

잘 작성된 커밋 메시지는 무엇일까? 여러가지 레퍼런스를 찾아보니 다양한 규칙이 있었다.

인터넷을 찾아보면 크게 작성 규칙과 타입을 작성하는 규칙이 가장 많이 나온다.

### 작성 규칙

1. 제목과 본문을 빈 행(한 줄 띄우기)으로 구분
2. 제목을 50자 내로 제한
3. 제목 첫 글자는 대문자로 작성
4. 제목 끝에 마침표 넣지 않기
5. 제목은 명령문으로 사용하며 과거형을 사용하지 않기
6. 본문의 각 행은 72글자 내로 제한
7. 어떻게 보다는 무엇(What)과 왜(How)를 설명

이런 규칙이 가장 많이 보편화 되어있고 나오는 듯 하다.

규칙을 읽어보면 알다시피 영문을 기준으로 하는 것 같고, 나머지는 팀별 규칙에 따라 유연성을 가지고 참고하면 될 것 같다.

### 타입 규칙

1. feat (feature) - 새로운 기능 추가
2. fix (bug fix) - 버그 픽스
3. docs (documentation) - 문서 수정
4. style (formatting, missing semi colons, …) - 코드 로직의 변경 없이, 스타일과 포맷팅의 변화만 줄 경우
5. refactor - 코드 리팩토링
6. test - 테스트 코드
7. chore (maintain) - 빌드, 패키지 등

주로 커밋 메시지의 제목 앞에 타입을 명시하고 해당 커밋이 무슨 일을 하는지 바로 알려주는 역할을 한다.

나는 GUI툴을 사용하다보니 해당 타입들만 잘 지켜도 보기 편해지겠다.

## 어떻게 작성할까

대충 어떻게 사용할 지에 대한 규칙을 정했다면 작성법만 정하면 된다.
일단 개인적으로 쓰나 팀으로 쓰나, 글자 수라던가에 대한 규칙까지 정할 필요는 없다고 생각했다.
가장 중요하게 생각하는 제목에 타입만 잘 적어도 한결 도움되지 않을까 해서 정해보았다.

```
[feat] 자동완성 기능 추가

통합검색 부분에 자동완성 기능을 추가한다.

- 본문검색 X
- 키워드 검색 위주
```

위의 예시정도만 지켜서 사용해보자.

## 적용하고 몇개월간 사용해봤더니 장단점

확실히 처음 생각처럼 과거코드를 살펴보거나 해당 커밋의 내용을 볼 때는 편해졌다.
근데 풀리퀘스트를 이용해서 머지를 하게 되면 깃랩, 깃허브의 merge 커밋이 생기는데 해당 커밋 메시지까지 수정이 가능한지 잘 모르겠다.
어떻게 해야 잘 관리할수 있을지는 좀 더 공부를 해야겠다. 그래프의 그림도 이쁘게 만드려면 git 공부를 더 해야겠다.
