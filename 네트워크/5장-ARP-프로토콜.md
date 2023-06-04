### [ARP 프로토콜](https://youtu.be/LDsp-Xb168E?list=PL0d8NnikouEWcF1jJueLdjRIC4HsUlULi)

같은 네트워크 대역에서 통신을 하기 위해 필요한 **MAC 주소를 IP 주소를 이용해서 알아오는 프로토콜**

보안상 중요하게 여겨짐, 

- ARP 프로토콜의 구조
![Untitled](../img/%EC%8A%A4%ED%81%AC%EB%A6%B0%EC%83%B7%202023-06-05%20%EC%98%A4%EC%A0%84%2012.51.44.png)

### ARP 프로토콜의 통신 과정

**1.** 송신자는 목적지 IP Address를 지정해 패킷을 송신

**2.** IP 프로토콜이 ARP 프로토콜에게 ARP Request 메시지를 생성하도록 요청

**3.** 메시지는 데이터링크 계층으로 전달되고 이더넷 프레임으로 Encapsulation됨

**4.** 모든 호스트와 라우터는 프레임을 수신 후 자신의 ARP 프로토콜에게 전달

**5.** 목적지 IP Address가 일치하는 시스템은 자신의 물리주소를 포함하고 있는 ARP Reply 메시지를 보냄

**6.** 최초 송신 측은 지정한 IP Address에 대응하는 물리주소를 획득

### ARP 테이블

통신했던 컴퓨터들의 주소는 ARP 테이블에 남는다

캐시라 일정 시간 뒤면 사라짐

### [ARP 프로토콜 실습](https://youtu.be/-M_S50Ga384?list=PL0d8NnikouEWcF1jJueLdjRIC4HsUlULi)

