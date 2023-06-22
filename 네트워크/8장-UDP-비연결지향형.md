### [UDP 프로토콜](https://youtu.be/3MkI3FBFzX8?list=PL0d8NnikouEWcF1jJueLdjRIC4HsUlULi)

**사용자 데이터그램 프로토콜**은 **유니버설 데이터그램 프로토콜**이라고 일컫기도 한다.

udp의 전송방식은 너무 단순해서 서비스의 신뢰성이 낮고, 데이터그램 도착 순서가 바뀌거나, 중복되거나, 통보 없이 누락시키기도 함 

오류의 검사와 수정이 필요없는 프로그램에서 수행할 것으로 가정한다.

- 구조
    
    ![Untitled](../img/%EC%8A%A4%ED%81%AC%EB%A6%B0%EC%83%B7%202023-06-20%20%EC%98%A4%ED%9B%84%203.48.35.png)
    
- udp 프로토콜을 사용하는 프로그램
    - **DNS 서버**: 도메인을 물으면 IP 알려줌
    
    ![Untitled](../img/%EC%8A%A4%ED%81%AC%EB%A6%B0%EC%83%B7%202023-06-20%20%EC%98%A4%ED%9B%84%203.53.48.png)
    
    - **tftp 서버**: udp로 파일을 공유
    - RIP 프로토콜: 라우팅 정보를 공유
        


### [tftpd로 파일 전송 실습](https://youtu.be/5Woau-EJChw?list=PL0d8NnikouEWcF1jJueLdjRIC4HsUlULi)

1. tftpd 를 사용해 데이터 공유하기
2. 패킷 캡쳐 및 분석해보기