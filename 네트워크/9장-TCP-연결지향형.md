### [TCP 프로토콜](https://youtu.be/cOK_f9_k_O0?list=PL0d8NnikouEWcF1jJueLdjRIC4HsUlULi)

- 전송제어프로토콜은 인터넷에 연결된 컴퓨터에서 실행되는 프로그램 간에 통신을 **안정적으로, 순서대로, 에러없이** 교환할 수 있게 한다.

TCP는 UDP보다 안전하지만 느리다.

- tcp 구조

![Untitled](../img/%EC%8A%A4%ED%81%AC%EB%A6%B0%EC%83%B7%202023-06-23%20%EC%98%A4%ED%9B%84%202.44.21.png)

- Offset : ip는 헤더의길이 4로 나눠서 작성, 얘도 똑같다 offset에 작성
- Reserved: 예약된 필드로 사용되지 않는다.
- Checksum
- window: tcp는 연결지향, 데이터 얼마만큼 더 보내!, 내 남은 tcp buffer 공간 알려줌
- urgent pointer

### TCP 플래그

- U : Urgent flags  긴급 비트, 우선순위가 높다
- A : Ack flag 승인비트, 물어본것에 응답을 해줄때
- P : Push flag, 버터 공간 상관없이 계속 받겠다
- R : Reset 초기화 비트, 우리 연결 관계를 새로고침하자 (문제 시)
- **S** : Sink bit , 상대방이랑 연결을 시작할때 사용, 동기화 비트
- F : fin bit ,  종료 비트, 연결을 끊을 때

### [TCP 3Way Handshake](https://youtu.be/Ah4-MWISel8?list=PL0d8NnikouEWcF1jJueLdjRIC4HsUlULi)

- TCP 를 이용한 통신과정
    - 연결 수립 과정
        - TCP 를 이용한 데이터 통신을 할 때 프로세스와 프로세스를 연결하기 위해 가장 먼저 수행되는 과정
            1. 클라이언트가 서버에게 요청 패킷을 보내고
            2. 서버가 클라이언트의 요청을 받아들이는 패킷을 보내고
            3. 클라이언트는 이를 최종적으로 수락하는 패킷을 보낸다
            
            위의 3개의 과정을 **3Way HandShake** 라고 부른다
        ![Untitled](../img/%EC%8A%A4%ED%81%AC%EB%A6%B0%EC%83%B7%202023-06-29%20%EC%98%A4%ED%9B%84%2012.40.36.png)

연결 수립 후 다시 클라이언트로부터 요청

### [TCP를 이용한 데이터 전송 과정](https://youtu.be/0vBR666GZ5o?list=PL0d8NnikouEWcF1jJueLdjRIC4HsUlULi)

- 데이터 송수신 과정
    - tcp 를 이용한 데이터 통신을 할 때 단순히 tcp 패킷만을 캡슐화해서 통신하는 것이 아닌 페이로드를 포함한 패킷을 주고 받을 떄의 일정한 규칙
        1. 보낸 쪽에서 또 보낼때는 SEQ 번호와 ACK 번호가 그대로다
        2. 받는 쪽에서 SEQ 번호는 받은 ACK 번호가 된다
        3. 받는 쪽에서 ACK 번호는 받은 SEQ 번호 + 데이터 크기
        
        ![Untitled](../img/%EC%8A%A4%ED%81%AC%EB%A6%B0%EC%83%B7%202023-06-29%20%EC%98%A4%ED%9B%84%2012.57.46.png)

### [TCP의 연결 상태 변화](https://youtu.be/yY0uQf0BTH8?list=PL0d8NnikouEWcF1jJueLdjRIC4HsUlULi)

- TCP 상태전이도
    - TCP 연결 상태의 변화
        - 실선: 클라이언트의 상태변화
        - 점선: 서버의 상태변화

![Untitled](../img/%EC%8A%A4%ED%81%AC%EB%A6%B0%EC%83%B7%202023-06-29%20%EC%98%A4%ED%9B%84%201.29.38.png)
서버 : passive open
클라이언트: active open