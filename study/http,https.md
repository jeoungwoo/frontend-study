## 📝http, https?

먼저, http 란?

HTTP(Hyper Text Transfer Protocol)란 서버/클라이언트 모델을 따라 데이터를 주고 받기 위한 프로토콜이다.
즉, HTTP는 인터넷에서 하이퍼텍스트를 교환하기 위한 통신 규약으로, 80번 포트를 사용하고 있다. 따라서 HTTP 서버가 80번 포트에서 요청을 기다리고 있으며, 클라이언트는 80번 포트로 요청을 보내게 된다.

http 의 구조

![image](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FbkdJ4Q%2FbtqK6AXLEtC%2FjBZzMuJBWzdLYmqILo5Ri1%2Fimg.png)

하지만 HTTP는 암호화가 되지 않은 평문 데이터를 전송하는 프로토콜이였기 때문에, HTTP로 비밀번호나 주민등록번호 등을 주고 받으면 제3자가 정보를 조회할 수 있었다. 그리고 이러한 문제를 해결하기 위해 HTTPS가 등장하게 되었다.

그렇다면, https 란?

HyperText Transfer Protocol over Secure Socket Layer, HTTP over TLS, HTTP over SSL, HTTP Secure 등으로 불리는 https는 http에 데이터 암호화가 추가된 프로토콜이다. https는 http와 다르게 443번 포트를 사용하며, 네트워크 상에서 중간에 제3자가 정보를 볼 수 없도록 공개키 암호화를 지원하고 있다.

https는 공개키/개인키 암호화 방식을 이용해 데이터를 암호화하고 있다. 공개키와 개인키는 서로를 위한 1쌍의 키이다.

• 공개키: 모두에게 공개가능한 키

• 개인키: 나만 가지고 알고 있어야 하는 키

![image](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FOKcog%2FbtqK71fM8a4%2Fg1HmcDOR7MVRRz7pSKKJWk%2Fimg.png)

### 정리

http는 암호화가 추가되지 않았기 때문에 보안에 취약한 반면, https는 안전하게 데이터를 주고받을 수 있다. 하지만 https를 이용하면 암호화/복호화의 과정이 필요하기 때문에 http보다 속도가 느리다.(오늘날에는 거의 차이를 못느낄 정도이다.) 또한 https는 인증서를 발급하고 유지하기 위한 추가 비용이 발생하다.

그렇다면 언제 http를 쓰고, 언제 https를 쓰는 것이 좋을까?

개인 정보와 같은 민감한 데이터를 주고 받아야 한다면 https를 이용해야 하지만, 단순한 정보 조회 등만을 처리하고 있다면 http를 이용하면 된다.
