# Network

### OSI 7 layers
  - **OSI 7 계층을 분리시켜놓은 이유**
  - **OSI 7 Layer**
### TCP/IP 4 Layer , TCP/IP 5 Layer
  - **TCP/IP 4 Layer**
  - **TCP/IP 5 Layer**
### Application Layer
  - **HTTP**
  - **HTTPS**
  - **DNS**
### Presentation Layer
  - **대칭키 & 공개키**
  - **SSL/TLS**
### Session Layer
  - **Cookie Session**
### Transport Layer
  - **TCP**
  - **UDP**
### Network Layer
  - **IP**
### 로드 밸런싱(Load Balancing)
### REST and RESTful
### CORS
### 웹 통신 전체 흐름
<br>


## OSI 7 layers
  #### OSI 7 계층을 분리시켜놓은 이유 : 
    - 통신이 일어나는 과정을 단계적으로 파악.
    - 통신 과정 중 이상이 생길 경우 통신 장애를 일으킨 계층에서 다른 계층에 영향을 주지 않고 해결하기 위함.

  #### OSI 7 Layer
    응용 계층(Application Layer) : 전송 단위 - Message
      - 응용 프로세스와 직접 관계하여 일반적인 응용 서비스를 수행하는 계층.
      - 주요 프로토콜 : FTP, Telnet, SSH, DNS, HTTP 등
      
    표현 계층(Presentation Layer) : 전송 단위 - Message
      - 응용프로그램이나 네트워크를 위해 데이터를 표현하는 계층.
      - 주요 프로토콜 : JPEG, MPEG 등
      
    세션 계층(Session Layer) : 전송 단위 - Message
      - 양 끝단의 응용 프로세스가 통신을 관리하는 방법을 제공하는 계층.
      - 네트워크상의 논리적인 연결을 관리하고 지속
      
    전송 계층(Transport Layer) : 전송 단위 - TCP 일 때 Segment / UDP 일 때 Datagram
      - 통신을 활성화하기 위한 계층.
      - 데이터 경로인 포트를 관리하여 전송에 도움을 준다.
      - 주요 프로토콜 : TCP, UDP
      
    네트워크 계층(Network Layer) : 전송 단위 - Packet
      - 데이터의 경로를 선택, 주소를 정하고 경로에 따라 패킷을 전달해주는 계층.
      - 데이터를 목적지까지 가장 안전하고 빠르게 전달.
      - 대표 장치 : 라우터
      - 주요 프로토콜 : IP, ICMP, IRMP, ARP 등
      
    데이터 링크 계층(Data link Layer) : 전송 단위 - Frame
      - 물리 계층을 통해 송수진되는 정보의 오류와 흐름을 관리하여 안전한 정보의 전달을 수행하는 역할.
      - 통신에서의 오류 발견 및 재전송.
      - 대표 장치 : 브리지, 스위치 등
      - 주요 프로토콜 : HDLC, Ethernet, PPP 등
      
    물리 계층(Physical Layer) : 전송 단위 - Bit
      - 실제 장치를 연결하기 위한 전기적 및 물리적 세부 사항을 정의한 계층.
      - 단지 데이터를 전달만 할 뿐 주고받는 데이터가 무엇인지, 어떤 에러가 있는지 등은 신경쓰지 않고 전기적인 신호로 변환한다.
      - 대표 장치 : 리피터, 케이블, 허브 등


## TCP/IP 4 Layer , TCP/IP 5 Layer
  #### TCP/IP 4 Layer
    - TCP/IP 4 Layer는 OSI 7 Layer보다 먼저 개발된 초기 모델.
    - 미국 국방부(DoD)에서 정의한 네트워크 통신 표준 모델.
    - OSI 7 Layer와 달리 이름에서 볼 수 있듯 4개의 계층으로 이루어져 있다.
    - 인터넷 개발 이후 계속 표준화되어 신뢰성이 우수.
  
    
    응용 계층(Application Layer) : 전송 단위 - Date / Message
      - OSI 7 Layer의 상위 3계층(응용, 표현, 세션)에 해당하며 각 계층의 기능을 제공하는 계층.
      - 응용 프로그램 간의 데이터 통신을 위해 사용하는 프로토콜을 정의.
      
    전송 계층(Transport Layer) : 전송 단위 - Segment
      - OSI 7 Layer의 4계층(전송)에 해당하며 각 계층의 기능을 제공하는 계층.
      - 통신 노드 간의 연결제어 및 자료의 송수신을 담당. (Transport Layer)
      
    인터넷 계층(Internet Layer) : 전송 단위 - Packet
      - OSI 7 Layer의 3계층(네트워크)에 해당 및 기능을 제공하는 계층.
      - 논리적 주소인 IP를 이용한 노드간 전송과 라우팅 기능을 처리하며, 네트워크상 목적지까지 연결성을 제공한다. (Network Layer)
      
    네트워크 인터페이스 계층(Network Interface Layer) : 전송 단위 - Frame
      - OSI 7 Layer의 1, 2계층(물리, 데이터링크)에 해당하며 각 계층의 기능을 제공하는 계층.
      - 물리적인 네트워크 통신을 정의하며, 흐름 제어(Flow Control)는 Header(MAC)에서 수행한다. (Physical Layer)
      - 에러검출과 패킷의 프레임화 역할을 담당하며, 에러 제어(Error Control)는 Tailer(CRC)에서 수행한다. (Data link Layer)

      
  #### TCP/IP 5 Layer
    - 인터넷 개발 이후 꾸준히 표준이 갱신되면서 TCP/IP 4 Layer의 하위 계층이 다시 세분화되어 개발된 모델.
    - TCP/IP 4 Layer의 가장 하위 계층인 '네트워크 인터페이스' 계층을 '데이터 링크' 계층과 '물리' 계층으로 세분화.
    - TCP/IP 4 Layer의 '인터넷' 계층의 명칭을 OSI 7 Layer와 같은 '네트워크' 계층으로 변경.
    - 현재 전 세계 표준 모델로 적용.


## Application Layer
  #### HTTP
    HTTP(HyperText Transfer Protocol)
    - 인터넷 상에서 클라이언트와 서버가 자원을 주고 받을 때 쓰는 통신 규약.
    - 사용자가 웹 사이트를 방문하면 사용자 브라우저가 웹 서버에 HTTP 요청을 전송하고 웹 서버는 HTTP 응답으로 응답.
    - HTTP 프로토콜은 네트워크 통신을 작동하게 하는 기본 기술.
    - 비연결성, 무상태성
    
    Method
      - 클라이언트와 서버 사이에 이루어지는 요청(Request)과 응답(Response) 데이터를 전송하는 방식.
      - 서버에 주어진 리소스에 수행하길 원하는 행동, 서버가 수행해야 할 동작을 지정하는 요청을 보내는 방법.
      - GET
        리소스 조회 메서드 (Read)
        조회할 때 POST도 사용할 수 있지만, GET 메서드는 캐싱이 가능하기에 GET을 사용하는 것이 유리하다.
      - POST
        전달한 데이터 처리/생성 요청 메서드 (Create)
        메시지 바디(body)를 통해 서버로 요청 데이터 전달하면 서버는 요청 데이터를 처리하여 업데이트
      - 그 외
        - PUT
          리소스를 대체(수정)하는 메서드 (Update)
        - PATCH
          리소스 일부 부분을 변경하는 메소드 (Update)
        - DELETE
          리소스 제거하는 메소드 (Delete)

      - HTTP 상태 코드
        1xx(정보) : 요청을 받았으며 프로세스를 계속 진행
        2xx(성공) : 요청을 성공적으로 받았으며 인식했고 수용
        3xx(리다이렉션) : 요청 완료를 위해 추가 작업 조치가 필요
        4xx(클라이언트 오류) : 요청의 문법이 잘못되었거나 요청을 처리할 수 없음
        5xx(서버 오류) : 서버가 명백히 유효한 요청에 대한 충족을 실패

        
  #### HTTPS
    HTTPS(HyperText Transfer Protocol Secure)
    - 인터넷 상에서 정보를 암호화하는 SSL 프로토콜을 사용해 클라이언트와 서버가 자원을 주고 받을 때 쓰는 통신 규약.
    
  #### DNS
    DNS 흐름


## Presentation Layer
  #### 대칭키 & 공개키
  #### SSL/TLS


## Session Layer
  #### Cookie Session


## Transport Layer
  #### TCP
    - 클라이언트와 서버가 연결된 상태에서 데이터를 주고받는 연결 지향 프로토콜.
    - 클라이언트 측에서 서버 측에 연결 요청과 서버 측의 연결 수락으로 통신 선로 고정, 고정 선로로 데이터 순차 전송.
    - 위와 같은 이유로 UDP와 달리 데이터를 정확하고 안정적으로 전송 가능. (신뢰성있는 데이터 전송)
    - 연결 설정(3 way handshake) 및 해제(4 way handshake).
    - 데이터 흐름 제어 및 혼잡 제어 기능 제공.

  #### TCP 3 way handshake
    - 서로의 통신을 위한 관문(port)을 확인하고 연결하기 위해 발생하는 3번의 요청/응답.
    1. 클라이언트에서 서버(Listen 상태)로 연결을 하기 위해 SYN(연결 요청 플래그) 패킷을 송신.
    2. 서버에서 SYN 패킷을 수신 후 SYN_RCV 상태로 전환.
    3. 서버에서 클라이언트로 SYN에 대한 응답인 ACK(응답플래그) 패킷 및 포트 오픈 요청으로 SYN 패킷을 함께 송신.
    4. 클라이언트에서 SYN + ACK 패킷을 수신 후 ESTABLISHED 상태로 전환 및 서버로 SYN에 대한 응답인 ACK 송신.
    5. 서버에서 클라이언트 측의 ACK 패킷을 수신하고 ESTABLISHED 상태로 전환.
        -> 클라이언트와 서버 연결.

  #### TCP 4 way handshake
    - 연결 해제를 위해 발생하는 4번의 요청/응답.
    1. 클라이언트에서 서버와의 연결 종료를 위해 서버에 FIN(연결 해제 플래그) 패킷을 송신하고 FIN_WAIT1 상태로 전환.
    2. 서버는 클라이언트로부터 FIN을 수신 후 응답 패킷 ACK을 송신하고 상태는 CLOSE_WAIT으로 전환.
    3. 서버가 통신이 끝나면, 즉 연결을 종료할 준비가 되면 클라이언트에게 FIN패킷을 보내고 LAST_WAIT 상태로 전환.
    4. 클라이언트는 확인 패킷 ACK을 보내고 TIME_WAIT 상태로 전환.
        -> 클라이언트와 서버 연결 해제.

  #### 흐름 제어
    - 기본 개념은 수신자가 송신자에게 현재 자신의 상태를 feedback 한다는 점.
    - Stop and Wait
    - Sliding Window
  #### 혼잡 제어
    - 송신측의 데이터 전달과 네트워크의 데이터 처리 속도 차이를 해결하기 위한 기법.
    - 네트워크 내에 패킷의 수가 과도하게 증가하는 현상을 혼잡이라 하며, 혼잡 현상을 방지하거나 제거하는 기능.
    - AIMD(Additive Increase / Multiplicative Decrease)
    - Slow Start(느린 시작)
    - Congestion Avoidance(혼잡 회피)
    - Fast Retransmit (빠른 재전송)
    - Fast Recovery (빠른 회복)
  #### 오류 제어
    - Stop and Wait ARQ
    - Go Back N ARQ
    - Selective Repeat ARQ(SR ARQ)
    - Adaptive ARQ

  #### UDP
    - 데이터를 주고받을 때 연결 절차를 거치지 않고 발신자가 일방적으로 데이터를 발신하는 비연결 지향 프로토콜.
    - 데이터그램 단위로 쪼개면서 전송을 해야하기 때문에 전송 계층에서 사용하는 프로토콜.
    - 데이터의 신속성. 데이터의 처리가 TCP보다 빠르다.


## Network Layer
  #### IP
    Socket
    WebSocket


## 로드 밸런싱(Load Balancing)


## REST and RESTful


## CORS
  Cross-Origin Resource Sharing(교차 출처 리소스 공유 정책)
    -> Origin : Protocol + Host + Port
  다른 출처의 리소스 공유에 대한 허용/비허용 정책.
  SOP 정책을 위반해도 CORS 정책에 따르면 다른 출처의 리소스라도 허용.

## 웹 통신 전체 흐름
