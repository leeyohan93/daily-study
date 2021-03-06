# RESTful API

## RESTful API란 무엇인가?
REST란 모든 자원(이미지, 동영상, DB 자원)에 고유한 URI를 부여해 활용하는 것이다. Restful API는 REST 아키텍쳐 스타일을 따르는 API를 말한다.
- 웹과 같은 분산 하이퍼미디어 시스템을 위한 아키텍쳐 스타일(제약조건의 집합)
- 모바일과 같은 다양한 클라이언트의 등장으로 Backend 하나로 다양한 Device를 대응하기 위해 REST의 개념이 대두되었습니다.

## REST 구성요소
- 자원(HTTP URI), 행위(HTTP Method), 표현방식(MINE Type)

## REST 제약 조건
- How do I improve HTTP without breaking the Web.
- 대부분은 **uniform interface의 self-descriptive와 HATEOAS를 거의 만족하지 못하고 있다.**

1.  유니폼 인터페이스 : 자원은 유일하게 식별가능해야하고, HTTP Method로 표현을 담아야 하고, 메세지는 스스로를 설명

2. 무상태성 : HTTP와 같이 상태정보를 따로 저장하고 관리하지 않고, API 서버는 들어오는 요청만을 단순 처리하면 된다.

3. 캐시가능 : HTTP가 가진 가장 강력한 특징 중의 하나인 캐싱 기능을 적용할 수 있다.

4. 클라이언트-서버: REST 서버는 API 제공, 클라이언트는 사용자 인증이나 컨텍스트(세션, 로그인 정보 등)을 직접 관리하는 구조로 각각의 역할이 확실히 구분되기 때문에 클라이언트와 서버에서 개발해야 할 내용이 명확해지고 서로간 의존성이 줄어들게 된다.

5. 계층형 구조: API 서버는 순수 비지니스 로직을 수행하고, 그 앞단에 사용자 인증, 암호화(ssl), 로드밸런싱 등을 하는 계층을 추가하여 구조상의 유연성을 둘 수 있다.

6. Code on demand(option) : 서버에서 코드를 클라이언트에게 보내서 실행하게 할 수 있어야 한다.

## 장점
- 메세지를 단순하게 표현 (쉽게 알아볼 수 있음)할 수 있다.
- 별도의 장비나 프로토콜이 필요없이 기존의 HTTP 인프라를 이용할 수 있다.
  (HTTP의 모범 사례)
- server, client를 독립적으로 구현할 수 있다.

## 참고
- https://brainbackdoor.tistory.com/53