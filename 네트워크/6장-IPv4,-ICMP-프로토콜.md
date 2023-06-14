### [IPv4 프로토콜](https://youtu.be/_i8O_o2ozlE?list=PL0d8NnikouEWcF1jJueLdjRIC4HsUlULi)

- 하는일
    
    네트워크 상에서 데이터를 교환하기 위한 프로토콜, **데이터가 정확하게 전달될 것을 보장하지 않음**.
    
    중복된 패킷을 전달하거나 패킷의 순서를 잘못 전달할 가능성 있음 (악의적으로 이용시 DoS 공격)
    
    → 데이터의 정확하고 순차적인 전달은 그 상위 프로토콜인 TCP 에서 보장
    
- 구조
    
    ![Untitled](../img/Untitled.png)
    
    - Version : 무조건 4가 온다, 6 이 오는 경우 없음 ipv6 는 구조 자체가 다름
    - IHL: 헤더의 길이, 최소 20 byte ~ 60 byte 근데 4비트로 표현(0~15)하기 위해 /4 를 해준다. 16진수로
    - TOS : 0 써준다. 옛날거라 안씀, 중요한 데이터임을 나타낸다
    - Total length : 뒤에 페이로드까지 합친 길이, 상위계층부터 인캡슐레이션한 전체의 길이
    - Identification + IP Flags  + Fragment Offset : 한세트, 데이터가 쪼개졌을때 알아볼 수 있는 값
    - TTL : 패킷이 살아있는 시간(숫자) 장비 넘어갈때마다 -1이 된다. N → 0 이 되는 순간 패킷 죽음, 운영체제마다 다름 윈도우 128, 리눅스 64
    - Protocol : 상위 프로토콜 타입 알려줌 icmp = 01 tcp = 06 udp = 17
    - header checksum: 헤더의 오류 확인

### [ICMP 프로토콜](https://youtu.be/JaBCIUsFE74?list=PL0d8NnikouEWcF1jJueLdjRIC4HsUlULi)

- 하는일
    
    Internet Control Message Protocol, 인터넷 제어 메시지 프로토콜
    
    네트워크 컴퓨터 위에서 돌아가는 운영체제에서 **오류 메시지**를 전송받는데 주로 쓰임
    
    프로토콜 구조의 Type 과 Code 를 통해 오류 메시지를 전송 받는다.
    
- 구조
    
    ![Untitled](../img/%EC%8A%A4%ED%81%AC%EB%A6%B0%EC%83%B7%202023-06-14%20%EC%98%A4%ED%9B%84%204.20.13.png)
    
    - type : 카테고리, 대분류
        - 0 echo Reply : 응답
        - 3 Destination Unreachable : 오류, 목적지 도달 못함, 중간에 경로 잘못
        - 5 Redirect : 라우팅 테이블을 원격지에서 수정, 남에것 수정 가능
        - 8 Echo.  : 요청
        - 11 Time Exceded : 오류, 목적지 갔지만 응답x, 상대방 방화벽
    - code : 소분류

### [IPv4, ICMP프로토콜 실습](https://youtu.be/8ZwTvTuZlVw?list=PL0d8NnikouEWcF1jJueLdjRIC4HsUlULi)

- 

### [라우팅 테이블](https://youtu.be/CjnKNIyREHA?list=PL0d8NnikouEWcF1jJueLdjRIC4HsUlULi)

- 

### [라우팅 테이블 확인 실습](https://youtu.be/tVntagSJctc?list=PL0d8NnikouEWcF1jJueLdjRIC4HsUlULi)

- 

### [IPv4 조각화 이론](https://youtu.be/_AONcID7Sc8?list=PL0d8NnikouEWcF1jJueLdjRIC4HsUlULi)

- 

### [IPv4 조각화 실습](https://youtu.be/QKEL9aBgHtg?list=PL0d8NnikouEWcF1jJueLdjRIC4HsUlULi)

-