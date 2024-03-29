## Cookie
***
### 등장배경
***
HTTP는 인터넷 상에서 데이터를 주고 받기 위한 서버/클라이언트 모델을 따르는 프로토콜이다. <br>
* 클라이언트가 서버에게 요청을 보내면, 서버는 응답을 보냄으로써 데이터를 교환한다.
HTTP는 비연결성 및 무상태성이라는 특징을 가지고 있다.
* HTTP는 요청 처리 후 연결을 끊어버리기 때문에, 클라이언트의 상태 정보 및 현재 통신 상태가 남아있지 않다. 
이 비연결성의 장점은 서버의 자원 낭비를 줄일 수 있다는 것이다. <br>
하지만 비연결성은 우리가 로그인과 같은 일을 할 때 누가 로그인 중인지 클라이언트는 식별할 수 없다.

이와 같은 문제점을 해결하기 위해 Cookie와 Session이라는 기술을 활용한다.

### Cookie란?
***
Java에서 cookie는 웹 애플리케이션에서 사용되는 중요한 요소이다. <br>
쿠키는 클라이언트 측에서 상태 정보를 저장하기 위해 사용되며, 클라이언트 컴퓨터에 작은 테스트 파일로 저장된다. <br>
쿠키는 웹 페이지를 방문할 때마다 항상 서버로 전송된다.

`주의`
* 쿠키 정보는 항상 서버에 정송되기 때문에 네트워크 트래픽이 추가적으로 발생한다.
  - 최소한의 정보만 사용한다. ex) 세션ID, 인증 토큰
* 보안에 민감한 데이터는 저장하면 안된다.
  - 주민번호, 신용카드 번호 등

### 쿠키의 용도
***
* 쿠키는 주로 세 가지 목적을 위해 사용된다.
1. 세션 관리(Session management)
  - 서버에 저장해야 할 사용자 로그인 정보를 받을 수 있다.
2. 개인화(Personalization)
  - 사용자 선호, 테마 등의 세팅을 할 수있다.
3. 트래킹(Tracking)
  - 사용자 행동을 기록하고 분석하는 용도로 사용된다.

### Set-Cookie & Cookie 동작방식
* Set-Cookie HTTP 응답 헤더는 서버로부터 사용자 에이전트로 전송된다.
* 간단한 쿠키는 다음과 같이 설정될 수 있다.
`Set-Cookie: key-value 형식으로 문자열로 담는다.`
```http
HTTP/1.0 200 OK
Content-type: text/html
Set-Cookie: 01 Jul 2023 15:32:33 GMT;
```
서버는 클라이언트의 로그인 요청에 대한 응답을 작성할 때, 클라이언트 측에 저장하고 싶은 정보를 응답 헤더의 set-cookie에 담는다. <br>
이후 클라이언트가 재요청 할 때마다 저장된 쿠키를 요청 헤더의 cookie 에 담아 보낸다. <br>
서버는 쿠키에 담긴 정보를 바탕으로 해당 요청의 클라이언트가 누군지 식별 할 수 있다.

### 쿠키의 생명주기
***
* setMaxAge();
* Set-Cookie: max-age=3600(3600초)
* 세션 쿠기: 만료 날짜를 생략하면 브라우저 종료시 까지만 유지
* 영속 쿠키: 만료 날짜를 입력하면 해당 날짜까지 유지

### 보안 문제 (단점)
* 쿠키만 사용해서 로그인을 유지할 때 발생할 수 있는 보안 문제가 있다.
* 쿠키 값은 임의로 변경할 수 있다.
  - 클라이언트가 쿠키를 강제로 변경하면 다른 사용자가 된다.
* 쿠키에 보과노딘 정보는 훔쳐갈 수 있다.
  - 쿠키의 정보로 나의 로컬 PC가 털릴 수도 있고, 네트워크 전송 구간에서 털릴 수도 있다.
* 해커가 쿠키를 한번 훔쳐가면 평생 사용할 수 있다.

**대안**
* 쿠키에 중요한 값을 노출하지 않고, 사용자 별로 예측 불가능한 임의의 토큰(랜덤 값)을 노출하고, 서버에서 토큰과 사용자 id를 매핑해서 인식한다.
* 그리고 서버에서 토큰을 관리한다.
* 해커가 토큰을 털어가도 시간이 지나면 사용할 수 없도록 서버에서 해당 토큰의 만료시간을 짧게(예: 30분) 유지한다.
* 또는 해킹이 의심되는 경우 서버에서 해당 토큰을 강제로 제거한다.




















