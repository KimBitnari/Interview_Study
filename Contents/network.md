# 네트워크 Network

<details>
<summary><strong>TCP UDP 차이점이 무엇인가요?</strong></summary>  
<hr>
<ul><li>답변</li></ul>
<hr>
</details>


<details>
<summary><strong>HTTP responce 상태 코드에 대해 설명해보세요</strong></summary>  
<hr>
<ul><li>답변</li></ul>
<hr>
</details>


<details>
<summary><strong>HTTP 프로토콜이 무엇인가요?</strong></summary>  
<hr>
<ul><li>답변</li></ul>
<hr>
</details>


<details>
<summary><strong>HTTP와 HTTPS의 차이점(+ 통신 방식의 차이)이 무엇인가요?</strong></summary>  
<hr>
<ul><li>답변</li></ul>
<hr>
</details>


<details>
<summary><strong>HTTP의 비연결성을 해결하기 위한 방법을 설명해주세요</strong></summary>  
<hr>
<ul><li>답변</li></ul>
<hr>
</details>


<details>
<summary><strong>쿠키(Cookie)와 세션(Session)의 차이점에 대해서 설명해주세요</strong></summary>  
<hr>
<ul><li>답변</li></ul>
<hr>
</details>


<details>
<summary><strong>HTTP method에 대해 아는 만큼 설명해주세요</strong></summary>  
<hr>
<ul><li>답변</li></ul>
<hr>
</details>


<details>
<summary><strong>HTTP 1.0 / 1.1 / 2.0 / 3.0 의 차이점에 대해서 설명해주세요</strong></summary>  
<hr>
<ul><li>답변</li></ul>
<hr>
</details>


<details>
<summary><strong>GET과 POST 차이점이 무엇인가요?</strong></summary>  
<hr>
<ul><li>답변</li></ul>
<hr>
</details>


<details>
<summary><strong>RESTFUL API의 URL 네이밍 규칙에 대해 설명해보세요</strong></summary>  
<hr>
<ul><li>답변</li></ul>
<hr>
</details>

<details>
<summary><strong>주소창에 https://www&#46;naver&#46;com/을 입력했을 때 일어나는 과정을 설명해보세요</strong></summary>  
<hr>
  <ol>
    <li>사용자가 브라우저에 URL(www&#46;naver&#46;com)을 입력</li>
    <li>DNS 서버에 도메인 네임으로 서버의 진짜 주소를 찾음</li>
    <li>HTTP 프로토콜을 사용하여 HTTP 요청 메세지를 생성</li>
    <li>TCP/IP 연결을 통해 HTTP요청이 서버로 전송</li>
    <li>서버는 HTTP 프로토콜을 활용해 HTTP 응답 메세지를 생성</li>
    <li>TCP/IP 연결을 통해 요청한 컴퓨터로 전송</li>
    <li>도착한 HTTP 응답 메세지는 웹 페이지 데이터로 변환되고, 웹 브라우저에 의해 출력</li>
  </ol>
<hr>
</details>

<details>
<summary><strong>Rest와 RestAPI에 대해서 설명해주세요.</strong></summary>  
<hr>
<ul>
  <li>Rest
    <ul>
      <li>자원을 이름(자원의 표현)으로 구분하여 해당 자원의 상태(정보)를 주고 받는 모든 것</li>
      <li>HTTP URI(Uniform Resource Identifier)를 통해 자원(Resource)을 명시하고, HTTP Method(POST, GET, PUT, DELETE)를 통해 해당 자원에 대한 CRUD Operation을 적용하는 것을 의미</li>
    </ul>
  </li>
  
  <li>RestAPI
    <ul>
      <li>REST 기반으로 서비스 API를 구현한 것</li>
    </ul>
  </li>
</ul>
<hr>
</details>

<details>
<summary><strong>Restful이란 무엇인가요.</strong></summary>  
<hr>
<ul>
  <li>REST API의 설계 규칙에 따라 웹 서비스를 제공할 때, RESTful 하다고 할 수 있다.</li>
  <li>Restful 하지 못한 경우
    <ul>
      <li>CRUD 기능을 모두 POST로만 처리하는 API</li>
      <li>route에 resource, id 외의 정보가 들어가는 경우 (/students/updateName)</li>
    </ul>
  </li>
</ul>
<hr>
</details>

<details>
<summary><strong>CORS란 무엇이며 이것에 대해서 설명해보세요.</strong></summary>  
<hr>
<ul>
  <li>Cross Origin Resource Sharing</li>
  <li>출처(Origin)가 다를 때, 보안상의 이유로 HTTP 요청을 제한하는데, CORS는 추가 HTTP 헤더를 사용하여, 현재 실행 중인 웹 애플리케이션이 아닌 다른 출처의 자원에 접근할 수 있는 권한을 부여하도록 브라우저에 알려주는 것</li>
  <li>출처가 다르다는 것은 dominA.com에서 domainB.com의 자원을 요청하는 것으로, 프론트단에서 서버로 HTTP 요청을 보낼 때 흔히 볼 수 있다.</li>
</ul>
<hr>
</details>

<details>
<summary><strong>OSI 7계층과 그 존재 이유, TCP/IP 4계층에 대해 설명해보세요.</strong></summary>  
<hr>
<ul>
  <li>OSI 7계층
    <ol>
      <li>1계층 - 물리 계층 (Physical Layer)
        <ul>
          <li>물리 계층은 전기적, 기계적 기능적인 특성을 이용해서 장비로 데이터를 전송</li>
          <li>물리 계층에서 사용되는 통신 단위는 Bit로 1(On)과 0(Off)으로 나타낸다.</li>
          <li>물리 계층에서는 단지 데이터를 전달만 한다.</li>
          <li>전송할 때(또는 받을 때) 데이터가 무엇인지, 어떤 에러가 있는지 등에는 전혀 신경 쓰지 않는다. 정말 단순하게 데이터를 전기적인 신호로 변환해서 주고받는 기능만 할 뿐이다. 결국 물리 계층은 어떤 에러가 있는지 전혀 관여하지 않는다.</li>
          <li>PDU : 비트(Bit) / 프로토콜 : Modem, Cable, Fiber, RS-232C</li>
          <li>대표장비 : 허브, 리피터</li>
        </ul>
      </li>
      <li>2 계층 - 데이터 링크 계층 (Data Link Layer)
        <ul>
          <li>링크 계층은 네트워크 기기들 사이의 데이터를 전송하는 역할</li>
          <li>물리적인 연결을 통해 오류와 흐름을 관리하며 인접한 두 장치의 신뢰성 있는 정보 전송을 담당한다.</li>
          <li>프레임(Frame) 단위의 PDU, MAC주소와 제어정보를 전송, 헤더를 통해 캡슐화 또는 캡슐화 해제</li>
          <li>결국 링크 계층은 에러검출 / 재전송 / 흐름제어 역할을 한다.</li>
          <li>PDU : 프레임(Frame) / 프로토콜 : 이더넷, MAC, PPP, ATM, LAN, wifi</li>
          <li>대표장비 : 브릿지, 스위치</li>
        </ul>
      </li>
      <li>3 계층 - 네트워크 계층(Network Layer)
        <ul>
          <li>경로를 선택하고 주소를 정하고 경로에 따라 패킷을 전달해주는 것이 네트워크 계층의 역할</li>
          <li>네트워크 계층에는 데이터를 목적지까지 안전하고 빠르게 전달하는 라우팅 기능이 있다.</li>
          <li>패킷(Packet)단위의 PDU, 패킷은 목적지까지 경로를 설정, 헤더를 통해 캡슐화 또는 캡슐화 해제</li>
          <li>결국 네트워크 계층은 주소 부여(IP) / 경로 설정(Route) 역할을 한다.</li>
          <li>PDU : 패킷(Packet) / 프로토콜 : IP, ICMP 등</li>
          <li>대표장비 : 라우터, L3 스위치</li>
        </ul>
      </li>
      <li>4 계층 - 전송 계층(Transport Layer)
        <ul>
          <li>전송 계층은 통신을 활성화하기 위한 계층</li>
          <li>양 끝단(End-to-End)의 사용자들이 신뢰성있고 정확한 데이터를 주고 받게 해주는 역할</li>
          <li>데이터 전송을 위해 Port번호가 사용된다.</li>
          <li>세그먼트(Segement)단위의 PDU, 종단 간의 에러복구와 흐름제어 담당, 헤더를 통해 캡슐화 및 캡슐화 해제</li>
          <li>전송 계층은 패킷 생성(Assembly/Sequencing/Deassembly/Error detection/Request repeat/Flow control) 및 전송 역할을 한다.</li>
          <li>PDU : 세그먼트(Segment) / 프로토콜 : TCP, UDP, ARP, RTP</li>
          <li>대표장비 : 게이트웨이, L4 스위치</li>
        </ul>
      </li>
      <li>5 계층 - 세션 계층(Session Layer)
        <ul>
          <li>통신 세션을 구성하는 계층으로, 포트(Port) 기반으로 연결한다.</li>
          <li>연결 세션에서 데이터 교환과 에러 발생 시의 복구를 관리. 즉, 논리적인 연결을 담당</li>
          <li>통신장치 간 상호 작용 및 동기화를 제공한다.</li>
          <li>헤더를 통해 캡슐화 및 캡슐화 해제</li>
          <li>세션 계층은 통신을 하기 위한 세션을 확립 / 유지 / 중단 역할을 한다.</li>
          <li>PDU : 데이터(Data) / 프로토콜 : NetBIOS, SSH, TLS</li>
        </ul>
      </li>
      <li>6 계층 - 표현 계층(Presentation Layer)
        <ul>
          <li>표현 계층은 코드 간의 번역을 담당하여 사용자 시스템에서 데이터의 형식상 차이를 다루는 부담을 응용 계층으로부터 덜어준다.</li>
          <li>MIME 인코딩이나 암호화 등의 동작이 표현 계층에서 이루어짐 (해당 데이터가 TEXT인지, 그림인지, GIF인지 JPG인지의 구분 등이 표현 계층의 몫)</li>
          <li>표현 계층은 사용자의 명령어를 완성 및 결과 표현하며, 압축 / 암호화 역할을 한다.</li>
          <li>PDU : 데이터(Data) / 프로토콜 : JPG, MPEG, SMB, AFP</li>
        </ul>
      </li>
      <li>7 계층 - 응용 계층(Application Layer)
        <ul>
          <li>응용 계층은 사용자와 바로 연결되어 있으며 응용 SW를 도와주는 계층이다.</li>
          <li>사용자로부터 정보를 입력받아 하위 계층으로 전달하고 하위 계층에서 전송한 데이터를 사용자에게 전달한다.</li>
          <li>사용자와 가장 밀접한 계층, 인터페이스(Interface) 역할</li>
          <li>파일 전송, DB, 메일 전송 등 여러가지 응용 서비스를 연결해주는 역할을 한다.</li>
          <li>응용 계층은 응용 프로세스와 직접 관계하여 일반적인 응용서비스를 수행한다.</li>
          <li>PDU : 데이터(Data) / 프로토콜 : DHCP, DNS, FTP, HTTP</li>
        </ul>
      </li>
    </ol>
  </li>
  <li>OSI 7계층 존재 이유
    <ul>
      <li>통신이 일어나는 과정을 단계 별로 파악할 수 있기 때문</li>
      <li>7단계 중 특정한 곳에 이상이 생기면 다른 단계의 장비 및 소프트웨어를 건드리지 않고 이상이 생긴 단계만 고칠 수 있다.</li>
      <li>표준화를 통해 장비별 이질적인 포트, 프로토콜을 구별</li>
      <li>OSI 계층별 기능과 통신의 과정을 정립하여 교육하기 위한 목적</li>
    </ul>
  </li>
  <li>TCP/IP 4계층
    <ol>
      <li>L1 네트워크 연결 계층(Network Access Layer/Network Interface Layer)
        <ul>
          <li>데이터 단위: 프레임</li>
          <li>전송 주소: MAC</li>
          <li>물리적으로 데이타가 네트워크를 통해 어떻게 전송되는지를 정의</li>
          <li>논리주소(IP주소 등)가 아닌 물리주소(예. MAC주소(Media Access Control Address))을 참조해 장비간 전송</li>
          <li>기본적으로 에러검출/패킷의 프레임화 담당</li>
          <li>예시: MAC, LAN, 패킷망 등에 사용되는 것, Ethernet, PPP, Token Ring 등</li>
        </ul>
      </li>
      <li>L2 인터넷 계층(Internet Layer)
        <ul>
          <li>데이터 단위: 패킷</li>
          <li>전송 주소: IP</li>
          <li>네트워크상 최종 목적지까지 정확하게 연결되도록 연결성을 제공 및 IP 할당</li>
          <li>라우팅(Routing)기능, 즉 경로 설정 기능을 처리</li>
          <li>예시: IP, ARP, ICMP, RARP, OSPF</li>
        </ul>
      </li>
      <li>L3 전송 계층(Transport Layer)
        <ul>
          <li>데이터 단위: Segment</li>
          <li>전송 주소: Port</li>
          <li>통신 노드 간의 연결 제어 및 자료 송수신을 담당</li>
          <li>애플리케이션 계층의 세션과 데이터그램 통신서비스 제공</li>
          <li>예시: TCP, UDP, RTP, RTCP 등</li>
        </ul>
      </li>
      <li>L4 응용 계층(Application Layer)
        <ul>
          <li>데이터 단위: Data/Message</li>
          <li>사용자와 가장 가까운 계층으로 사용자가 소프트웨어 application과 소통할 수 있게 해준다</li>
          <li>응용프로그램(application)들이 데이터를 교환하기 위해 사용되는 프로토콜</li>
          <li>애사용자 응용프로그램 인터페이스를 담당</li>
          <li>예시: 파일 전송, 이메일, FTP, HTTP, SSH, Telnet, DNS, SMTP 등</li>
        </ul>
      </li>
    </ol>
  </li>
</ul>
<hr>
</details>

<details>
<summary><strong>SSL Handshake에 대해서 설명해보세요.</strong></summary>  
<hr>
<ol>
  <li>Client -> Server
    <ul>
      <li>Client hello 라고 불린다. 다음과 같은 데이터를 서버에 전송한다.</li>
      <li>클라이언트가 생성한 랜덤 데이터</li>
      <li>클라이언트가 지원하는 암호화 방식</li>
      <li>Session Id (이미 SSL handshake를 한번 완료했다면, 기존 session 재활용)</li>
    </ul>
  </li>
  <li>Server -> Client
    <ul>
      <li>Server hello 라고 불린다. 다음과 같은 데이터를 클라이언트에 전송한다.</li>
      <li>서버가 생성한 랜덤 데이터</li>
      <li>서버가 선택한 암호화 방식</li>
      <li>CA의 비밀키로 암호화 된 SSL 인증서</li>
    </ul>
  </li>
  <li>Client -> Server
    <ul>
      <li>클라이언트는 먼저 인증서를 발행한 CA를 신뢰할 수 있는지 판단한다. (갖고 있는 CA 리스트와 비교)</li>
      <li>진짜 그 CA가 발행한 인증서가 맞는지 확인한다.
        <ol>
          <li>기존에 갖고 있는 CA의 공개키를 사용해 인증서를 복호화 한다.</li>
          <li>복호화에 성공한다면, 신뢰 할 수 있는 CA가 보증한 서버임을 확신할 수 있다.</li>
          <li>공개키 방식을 거꾸로 사용해 Authentication에 활용했다고 할 수 있다.</li>
        </ol>
      </li>
      <li>이후 Client hello 의 랜덤 데이터와 Server hello 의 랜덤 데이터를 조합하여 pre master key 생성한다.</li>
      <li>pre master key를 암호화(인증서에 포함된 서버측 공개키 사용)하여 서버에 전송한다.</li>
    </ul>
  </li>
  <li>Pre master key를 session key로 변환
    <ul>
      <li>서버는 자신의 비밀키로 전달받은 pre master key를 복호화한다.</li>
      <li>클라이언트와 서버 모두 일련의 과정을 거쳐 세션 키를 획득한다. (pre master key -> master key -> session key)</li>
      <li>이후 세션 키를 대칭키로 사용해 데이터를 암호화 하여 클라이언트-서버 통신이 이루어진다.</li>
    </ul>
  </li>
  <li>Handshake 종료</li>  
</ol>
<hr>
</details>

<details>
<summary><strong>3-Handshaking과 4-Handshaking의 과정에 대해서 설명해보세요.</strong></summary>  
<hr>
<ol>
  <li>3-Handshaking
    <ul>
      <li>TCP 네트워크에서 통신을 하는 장치가 서로 연결이 잘 되었는지 확인하는 방법</li>
      <li>송신자와 수신자는 총 3번에 걸쳐 데이터를 주고 받으며 통신이 가능한 상태인지 확인</li>
    </ul>
  </li>
  <li>4-Handshaking
    <ul>
      <li>TCP 네트워크에서 통신 하는 장치의 연결을 해제하는 방법</li>
      <li>송신자와 수신자는 총 4번에 걸쳐 데이터를 주고 받으며 연결 끊음</li>
    </ul>
  </li>
</ol>
<hr>
</details>

<details>
<summary><strong>세션 기반 인증과 토큰 기반 인증의 차이는 무엇인가요?</strong></summary>  
<hr>
<ul>
  <li>세션 기반 인증은 클라이언트로부터 요청을 받으면 클라이언트의 상태 정보를 저장하므로 Stateful한 구조를 가진다.</li>
  <li>토큰 기반 인증은 상태 정보를 서버에 저장하지 않으므로 Stateless한 구조를 가진다.</li>
</ul>
<hr>
</details>

<details>
<summary><strong>JWT 토큰에 대해서 설명해주세요.</strong></summary>  
<hr>
<ul>
  <li>JWT는 JSON 포맷을 이용하는 Claim 기반의 웹 토큰이며, 토큰 자체를 정보로 사용하는 Self-Contained 방식으로 정보를 안전하게 전달</li>
  <li>JWT는 헤더(Header), 내용(Payload), 서명(Signature)로 구성되며, 각 파트를 점(.)으로 구분
    <ul>
      <li>헤더(Header) : 토큰의 타입과 해시 암호화 알고리즘(방식지정)으로 이루어져 있다.</li>
      <li>내용(Payload) : 토큰에 사용자가 담고자 하는 정보를 담는다. 내용에는 Claim이 담겨있고, JSON(Key/Value)형태의 한 쌍으로 이루어져 있다.</li>
      <li>서명(Signature) : 토큰을 인코딩하거나 유효성 검증할 때 사용하는 고유한 암호화 코드이다. 헤더와 내용의 값을 인코딩한다.</li>
    </ul>
  </li>
</ul>
<hr>
</details>

<details>
<summary><strong>대칭키, 비대칭키 암호화 방식에 대해서 설명해주세요.</strong></summary>  
<hr>
<ul>
  <li>대칭키와 비대칭키는 양방향 암호화 방식</li>
  <li>대칭키
    <ul>
      <li>대칭키는 암호화와 복호화에 같은 암호 키를 쓰는 알고리즘</li>
      <li>이는 중간에 누군가 암호 키를 가로채면 암호화된 정보가 유출될 수 있다는 단점이 있는데, 이런 문제를 보완한 새로운 방식이 비대칭키(공개키)</li>
    </ul>
  </li>
  <li>비대칭키
    <ul>
      <li>비대칭키는 암호화와 복호화할 때 키를 서로 다른 키로 사용하는 암호화 알고리즘</li>
      <li>타인에게 절대 노출되어서는 안되는 개인키(private key)와 공개적으로 개방되어 있는 공개키(public key)를 쌍으로 이룬 형태</li>
    </ul>
  </li>
</ul>
<hr>
</details>
