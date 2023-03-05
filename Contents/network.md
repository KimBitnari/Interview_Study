# 네트워크 Network

<details>
<summary><strong>TCP UDP 차이점이 무엇인가요?</strong></summary>  
<hr>
<ul>
  <li>TCP는 연결형 서비스로 3-way handshaking 과정을 통해 연결을 설정하기 때문에 높은 신뢰성을 보장하지만, 속도가 비교적 느리다는 단점이 있습니다.</li>
  <li>UDP는 비연결형 서비스로 3-way handshaking을 사용하지 않기 때문에 신뢰성이 떨어지는 단점이 있지만, 데이터 수신 여부를 확인하지 않기 때문에 속도가 빠르다는 장점이 있습니다.</li>
</ul>
<hr>
</details>


<details>
<summary><strong>HTTP responce 상태 코드에 대해 설명해보세요</strong></summary>  
<hr>
<ul><li>상태코드는 클라이언트가 서버를 향해 보낸 리퀘스트의 결과가 어떻게 되었는지 알려주는 역할을 합니다.</li>
  <li>1XX 코드는 리퀘스트를 받아들여 처리중을 나타냅니다.</li>
  <li>2XX 코드는 리퀘스트를 정상적으로 처리했음을 의미합니다.</li>
  <li>3XX 코드는 리퀘스트를 완료하기 위해 추가 동작이 필요함을 의미합니다.</li>
  <li>4XX 코드는 클라이언트의 원인으로 에러가 발생했음을 의미합니다.</li>
  <li>5XX 코드는 서버의 원인으로 에러가 발생했음을 의미합니다.</li>
</ul>
<hr>
</details>


<details>
<summary><strong>HTTP 프로토콜이 무엇인가요?</strong></summary>  
<hr>
<ul><li>데이터를 주고받기 위한 프로토콜이며 서버/클라이언트 모델을 따릅니다.</li></ul>
<hr>
</details>


<details>
<summary><strong>HTTP와 HTTPS의 차이점(+ 통신 방식의 차이)이 무엇인가요?</strong></summary>  
<hr>
<ul><li>HTTP는 평문 데이터를 전송하는 프로토콜이기 때문에, HTTP로 중요한 정보를 주고 받으면 제 3자에 의해 조회될 수 있습니다. 이러한 문제를 해결하기 위해 HTTP에 암호화가 추가된 프로토콜이 HTTPS입니다.</li>
  <li>HTTP는 원래 TCP와 직접 통신했지만, HTTPS에서 HTTP는 SSL과 통신하고 SSL이 TCP와 통신함으로써 암호화와 증명서, 안전성 보호를 이용할 수 있게 됩니다.</li>
  </ul>
<hr>
</details>


<details>
<summary><strong>HTTP의 비연결성을 해결하기 위한 방법을 설명해주세요</strong></summary>  
<hr>
<ul>
  <li>이러한 문제를 해결하기 위한 방법으로 Cookie 가 있습니다. 서버로부터 받은 쿠키정보를 클라이언트에 저장하고 다음번에 클라이언트가 같은 서버로 리퀘스트를 보낼 때 자동으로 쿠키값을 넣어서 송신합니다. 서버는 클라이언트가 보낸 쿠키값으로 클라이언트를 확인하고 서버상의 기록을 찾아 이전 상태를 알수있습니다.</li>
  <li>비연결성으로 인한 문제 : Http는 stateless 프로토콜로 과거의 request&respond 상태를 관리하지 않습니다. 이에 과거의 상태를 근거로 현재의 리퀘스트를 처리하는 것은 불가능합니다. 예를 들면, 인증이 필요한 웹 페이지의 상태를 관리하지 않으면 새로운 페이지로 이동할 때 마다 로그인 정보를 보내야합니다.</li>
  </ul>
<hr>
</details>


<details>
<summary><strong>쿠키(Cookie)와 세션(Session)의 차이점에 대해서 설명해주세요</strong></summary>  
<hr>
<ul>
  <li>쿠키는 접속자의 컴퓨터에 저장하는 작은 기록 정보 파일입니다. HTTP에서 클라이언트의 상태 정보를 PC에 저장했다가 필요시 정보를 참조하거나 재사용할 수 있습니다. 세션은 일정 시간동안 같은 사용자로부터 들어오는 일련의 요구를 하나의 상태로 보고, 그 상태를 유지시키는 기술입니다. 방문자가 웹 서버에 접속해 있는 상태를 하나의 단위, 세션이라 하고 웹 서버에 저장합니다.</li>
  <li>속도는 쿠키가 세션보다 빠르지만, 보안은 세션이 더 뛰어납니다.</li>
  </ul>
<hr>
</details>


<details>
<summary><strong>HTTP method에 대해 아는 만큼 설명해주세요</strong></summary>  
<hr>
<ul>
  <li>HTTP method는 클라이언트가 서버에게 사용자 요청의 목적을 알리는 방법입니다.</li>
  <li>GET : 데이터 조회</li>
  <li>POST : 데이터 등록</li>
  <li>PUT : 데이터 변경</li>
  <li>PATCH : 일부 데이터 변경</li>
  <li>DELETE : 데이터 삭제</li>
  </ul>
<hr>
</details>


<details>
<summary><strong>HTTP 1.0 / 1.1 / 2.0 / 3.0 의 차이점에 대해서 설명해주세요</strong></summary>  
<hr>
<ul>
  <li>HTTP 1.0 : 기본적으로 한 열결당 하나의 요청을 처리하도록 설계되어 있습니다.</li><br>
  <li>HTTP 1.1 : 요청이 있을 때 마다 매번 TCP 연결을 하는 것이 아니라, keep-alive라는 옵션으로 여러 개의 파일을 송수신할 수 있도록 변화했습니다. (1.0에서도 keep-alive가 있었지만, 표준화가 되어있지 않았고 1.1부터 표준화가 되어 기본 옵션으로 설정)</li>
  <ul>
    <li>HOL Blocking : 같은 큐에 있는 패킷이 그 첫 번째 패킷에 의해 지연될 때 발생하는 성능 저하 현상 ex. 여러 개의 파일을 순차적으로 다운 받을 때, 첫 번째 파일의 다운로드 속도가 느려지면, 뒤의 다른 파일 속도도 느려짐.</li>
 </ul><br>
  <li>HTTP 2.0 : 그 전 버전보다 지연 시간을 줄이고 응답 시간을 빠르게 할 수 있고 멀티플렉싱, 헤더 압축, 서버 푸시, 요청의 우선순위 처리를 지원합니다.</li>
  <ul>
  <li>멀티플렉싱 : 여러 개의 스트림을 사용하여 송수신. 특정 스트림의 패킷이 손실되었더라도 해당 스트림에만 영향을 미치고 나머지 스트림은 멀쩡하게 동작 → HTTP/1.x에서 발생하는 문제인 HOL Blocking 해결</li>
  <li>헤더 압축 : HTTP/1.x에는 헤더의 크기가 큰 문제가 있었습니다. HTTP/2에서는 허프만 코딩 압축 알고리즘을 사용해서 헤더 압축</li>
  <li>서버 푸시 : 1.1버전에서는 클라이언트가 서버에 요청을 해야 파일을 다운로드받을 수 있었지만, 2 버전은 클라이언트 요청 없이 서버가 바로 리소스를 푸시할 수 있음 → html 파일 요청이 들어오면, 그 안에 들어있던 css파일을 서버에서 푸시하여 클라이언트에 먼저 줄 수 있음</li>
 </ul><br>
  <li>HTTP 3.0 : TCP 위에서 돌아가는 HTTP/2와 달리 HTTP/3는 QUIC라는 계층 위에서 돌아가며, TCP 기반이 아닌 UDP 기반으로 돌아갑니다. → 3way handshake 필요 없음</li>

 </ul>
<hr>
</details>


<details>
<summary><strong>GET과 POST 차이점이 무엇인가요?</strong></summary>  
<hr>
<ul>
  <li>GET은 데이터를 조회하기 위해 사용되는 방식으로 데이터를 헤더에 추가하여 전송하는 방식입니다. URL에 데이터가 노출되므로 보안적으로 중요한 데이터를 포함해서는 안됩니다.</li>
  <li>POST는 보통 데이터를 등록하기 위해 사용되는 방식으로 데이터를 바디에 추가하여 전송하는 방식입니다. URL에 데이터가 노출되지 않아 GET 보다는 안전합니다.</li>
  </ul>
<hr>
</details>


<details>
<summary><strong>RESTFUL API의 URL 네이밍 규칙에 대해 설명해보세요</strong></summary>  
<hr>
<ul>
  <li>소문자 사용</li>
  <li>언더바(_) 사용 금지 대신 하이픈(-) 사용</li>
  <li>URI의 마지막에는 슬래시를 포함하지 않음</li>
  <li>계층관계를 나타낼 때는 슬래시 구분자 사용</li>
  <li>파일 확장자를 URI에 포함시키지 않음</li>
  <li>전달하고자 하는 자원의 명사를 사용, 컨트롤 자원을 의미하는 경우 예외적으로 동사를 허용 → 자원의 행위는 HTTP Method를 사용</li>
  <li>클라이언트 또는 서버에서 관리하는 리소스는 복수형으로 표현, 인스턴스는 단수로 표현 (ex. /users/:userIdx, /users/photo)</li>
  </ul>
<hr>
</details>

<details>
<summary><strong>주소창에 https://www&#46;naver&#46;com/을 입력했을 때 일어나는 과정을 설명해보세요</strong></summary>  
<hr>
  <ol>
    <li>사용자가 브라우저에 URL(www&#46;naver&#46;com)을 입력합니다.</li>
    <li>브라우저가 URL의 IP 주소를 찾기 위해 캐시에서 DNS 기록을 확인합니다.</li>
    <li>만약 요청한 URL이 캐시에 없다면, 도메인 이름(naver&#46;com)을 DNS 서버에서 검색하고, 해당하는 IP 주소를 찾아 사용자가 입력한 URL 정보와 함께 전달합니다.</li>
    <li>전달받은 정보들을 가지고 HTTP 프로토콜을 사용하여 HTTP 요청 메세지를 생성하고, TCP 프로토콜을 사용하여 웹서버에 HTTP 요청을 보냅니다.</li>
    <li>서버에 도착한 HTTP 요청 메세지는 웹 페이지 URL 정보로 변환되어 웹 페이지 URL 정보에 해당하는 데이터를 검색합니다.</li>
    <li>검색된 웹 페이지 데이터를 가지고 HTTP 프로토콜을 사용하여 HTTP 응답 메세지를 생성하고, TCP 프로토콜을 사용해 요청한 컴퓨터로 전송합니다.</li>
    <li>도착한 HTTP 응답 메세지는 웹 페이지 데이터로 변환되고, 웹 브라우저에 의해 출력됩니다.</li>
  </ol>
<hr>
</details>

<details>
<summary><strong>Rest와 RestAPI에 대해서 설명해주세요.</strong></summary>  
<hr>
<ul>
  <li>Rest는 자원(Resource)을 이름으로 구분해서 해당 상태를 주고 받는 것으로, HTTP URI를 통해 자원(Resource)을 명시하고, HTTP Method를 통해서 해당 자원에 대한 CRUD를 적용하는 것을 의미합니다.</li>
  <li>RestAPI는 REST를 기반으로 서비스 API를 구현한 것입니다.</li>
</ul>
<hr>
</details>

<details>
<summary><strong>Restful이란 무엇인가요.</strong></summary>  
<hr>
<ul>
  <li>REST API의 설계 규칙에 따라 웹 서비스를 제공할 때, RESTful 하다고 할 수 있습니다.</li>
  <li><참고> Restful 하지 못한 경우
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
  <li>cross origin이란 : 프로토콜, 도메인, 포트 번호, 이 중에서 한 가지라도 다른 경우</li>
  <li>추가 HTTP Header를 사용하여, 한 출처(origin)에서 실행 중인 웹 애플리케이션이 다른 출처의 선택한 자원에 접근할 수 있는 권한을 부여하도록 브라우저에 알려주는 것 입니다.</li>
  <li>CORS는 악의적으로 정보를 추출하거나 공격을 할 수 없도록 브라우저에서 보호하고, 필요한 경우에만 서버와 협의하여 요청할 수 있도록 하기 위해서 필요합니다.</li>
</ul>
<hr>
</details>

<details>
<summary><strong>OSI 7계층과 그 존재 이유, TCP/IP 4계층에 대해 설명해보세요.</strong></summary>  
<hr>
<ul>
  <li>OSI 7계층
    <ol>
      <li>1 계층 물리 계층(Physical Layer) : 전기적, 기계적, 기능적인 특성을 이용해서 통신 케이블로 데이터를 전송하는 물리적인 장비로, 데이터를 전기적인 신호(0,1)로 변환해서 주고받는 기능만 합니다.</li>
      <li>2 계층 데이터 링크 계층(Data Link Layer) : 물리 계층을 통해 송수신되는 정보의 오류와 흐름을 관리하여 안전한 통신의 흐름을 관리합니다.</li>
      <li>3 계층 네트워크 계층(Network Layer)으로 : 데이터를 목적지까지 가장 안전하고 빠르게 전달합니다. (라우터(Router)를 통해 경로를 선택하고 주소를 정하고(IP) 경로(Route)에 따라 패킷을 전달)</li>
      <li>4 계층 전송 계층(Transport Layer) : 두 지점간의 신뢰성 있는 데이터를 주고 받게 해주는 역할을 합니다. (port 번호, 전송방식(TCP/UDP) 결정)</li>
      <li>5 계층 세션 계층(Session Layer) : 양쪽 host 간에 최초 연결, 통신 중 연결이 끊어지지 않도록 유지시켜주는 역할을 합니다. (TCP/IP 세션 체결, 포트번호를 기반으로 통신 세션 구성)</li>
      <li>6 계층 표현 계층(Presentation Layer) : 전송하는 데이터의 표현방식을 결정합니다. (ex. 데이터변환, 압축, 암호화 등)</li>
      <li>7 계층 응용 계층(Application Layer) : 최종 목적지로, 응용 프로세스와 직접 관계하여 일반적인 응용 서비스를 수행합니다. (ex. explore, chrome 등)</li>
    </ol>
  </li>
  <br/>
  <li>OSI 7계층 존재 이유
    <ul>
      <li>통신이 일어나는 과정을 단계 별로 파악할 수 있고, 흐름을 한눈에 알아보기 쉽고, 사람들이 이해하기 쉽고, 7단계 중 특정한 곳에 이상이 생기면, 다른 단계의 장비 및 소프트웨어를 건드리지 않고 이상이 생긴 단계만 고칠 수 있기 때문입니다.</li>
    </ul>
  </li>
  <br/>
  <li>TCP/IP 4계층
    <ol>
      <li>L1 네트워크 연결 계층(Network Access Layer/Network Interface Layer)
        <ul>
          <li>OSI 7계층의 물리계층(1)과 데이터 링크 계층(2)에 해당</li>
          <li>TCP/IP 패킷을 네트워크 매체로 전달하는 것과 네트워크 매체에서 TCP/IP 패킷을 받아들이는 과정을 담당합니다.</li>
        </ul>
      </li>
      <li>L2 인터넷 계층(Internet Layer)
        <ul>
          <li>OSI 7계층의 네트워크 계층(3)에 해당</li>
          <li>네트워크상 최종 목적지까지 정확하게 연결되도록 연결성을 제공합니다.</li>
        </ul>
      </li>
      <li>L3 전송 계층(Transport Layer)
        <ul>
          <li>OSI 7계층의 전송 계층(4)에 해당</li>
          <li>통신 노드 간의 연결을 제어하고, 신뢰성 있는 데이터 전송을 담당합니다.</li>
        </ul>
      </li>
      <li>L4 응용 계층(Application Layer)
        <ul>
          <li>OSI 7계층의 세션 계층(5), 표현 계층(6), 응용 계층(7)에 해당</li>
          <li>다른 계층의 서비스에 접근할 수 있게 하는 애플리케이션을 제공하고, 애플리케이션들이 데이터를 교환하기 위해 사용하는 프로토콜을 정의합니다.</li>
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
  <li>서버는 CA에 사이트 정보와 공개 키를 전달하여 인증서를 받음</li>
  <li>클라이언트는 브라우저에 CA 공개 키가 내장되어 있다고 가정</li>
  <li>ClientHello : 암호화 알고리즘 나열 및 전달</li>
  <li>ServerHello : 암호화 알고리즘 선택</li>
  <li>Server Certificate : 인증서 전달</li>
  <li>Client Key Exchange : 데이터를 암호화 할 대칭 키 전달</li>
  <li>Client / ServerHello Done : 정보 전달 완료</li>
  <li>Finished : SSL Handshake 종료</li>
</ol>
<hr>
</details>

<details>
<summary><strong>3-way handshaking과 4-way handshaking의 과정에 대해서 설명해보세요.</strong></summary>  
<hr>
<ul>
  <li>TCP는 3-way handshaking 과정을 통해 연결 및 데이터를 수신받고, 4-way handshaking 과정을 통해 연결을 종료합니다.</li>
  <li>3-way handshaking
    <ol>
      <li>클라이언트는 서버에 접속을 요청하는 SYN 패킷을 전송합니다.</li>
      <li>서버는 SYN 요청을 받고, 클라이언트에게 요청을 수락한다는 SYN_ACK flag가 설정된 패킷을 전송합니다.</li>
      <li>클라이언트는 서버에게 ACK를 전송 후, 연결이 이루어지고 데이터가 오고 가게 됩니다.</li>
    </ol>
  </li>
  <li>4-way handshaking
    <ol>
      <li>클라이언트가 연결을 종료하겠다는 FIN 플래그를 전송합니다.</li>
      <li>서버는 확인메세지 ACK를 보낸 후, 자신의 통신이 끝날 때까지 기다립니다.</li>
      <li>서버의 통신이 끝났으면, 연결이 종료되었다고 클라이언트에 FIN 플래그를 전송합니다.</li>
      <li>클라이언트는 확인했다는 ACK를 보냅니다.</li>
    </ol>
  </li>
</ul>
<hr>
</details>

<details>
<summary><strong>세션 기반 인증과 토큰 기반 인증의 차이는 무엇인가요?</strong></summary>  
<hr>
<ul>
  <li>세션 기반 인증은 클라이언트로부터 요청을 받으면 클라이언트의 상태 정보를 저장하므로 Stateful한 구조를 가집니다.</li>
  <li>토큰 기반 인증은 상태 정보를 서버에 저장하지 않으므로 Stateless한 구조를 가집니다.</li>
</ul>
<hr>
</details>

<details>
<summary><strong>JWT 토큰에 대해서 설명해주세요.</strong></summary>  
<hr>
<ul>
  <li>JWT는 JSON 포맷을 이용하는 Claim 기반의 웹 토큰이며, 사용자를 인증하고 식별하기 위한 토큰 기반 인증입니다.</li>
  <li>JWT는 헤더(Header), 내용(Payload), 서명(Signature)로 구성되며, 각 파트를 점(.)으로 구분합니다.
    <ul>
      <li><참고></li>
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
  <li>대칭키와 비대칭키는 양방향 암호화 방식입니다.</li>
  <li>대칭키
    <ul>
      <li>대칭키는 암호화와 복호화에 같은 암호 키를 쓰는 알고리즘으로, 중간에 누군가 암호 키를 가로채면 암호화된 정보가 유출될 수 있다는 단점이 있습니다.</li>
      <li>이런 문제를 보완한 새로운 방식이 비대칭키(공개키)</li>
    </ul>
  </li>
  <li>비대칭키
    <ul>
      <li>비대칭키는 암호화와 복호화할 때 키를 서로 다른 키로 사용하는 암호화 알고리즘으로, 타인에게 절대 노출되어서는 안되는 개인키(private key)와 공개적으로 개방되어 있는 공개키(public key)를 쌍으로 이룬 형태입니다.</li>
    </ul>
  </li>
</ul>
<hr>
</details>
