# 데이터베이스 Database

<details>
<summary><strong>DB 정규화란?</strong></summary>  
<hr>
<ul>
  <li>하나의 릴레이션에 하나의 의미만 존재하도록 릴레이션을 분해하는 과정이며, 데이터의 일관성, 최소한의 데이터 중복, 최대한의 데이터 유연성을 위한 방법입니다.</li>
</ul>
<hr>
</details>


<details>
<summary><strong>정규화의 장단점?</strong></summary>  
<hr>
<ul>
  <li>장점
    <ol>
      <li>데이터베이스 변경 시 이상현상이 발생하는 문제점을 해결할 수 있습니다.</li>
      <li>데이터베이스 구조 확장 시 정규화된 데이터베이스는 그 구조를 변경하지 않아도 되거나 일부만 변경해도 됩니다.</li>
    </ol>
  </li>
  <li>단점
    <ol>
      <li>릴레이션의 분해로 인해 릴레이션 간의 연산(JOIN 연산)이 많아지는데, 이로인해 질의에 대한 응답 시간이 느려질 수 있습니다.</li>
    </ol>
  </li>
</ul>
<hr>
</details>


<details>
<summary><strong>역정규화를 하는 이유?</strong></summary>  
<hr>
<ul>
  <li>정규화를 거치면 릴레이션 간의 연산(JOIN 연산)이 많아지는데, 이로인해 성능이 저하될 우려가 있습니다.</li>
  <li>역정규화를 하는 가장 큰 이유는 성능 문제가 있는(읽기작업이 많이 필요한) DB의 전반적인 성능을 향상시키기 위함입니다.</li>
</ul>
<hr>
</details>


<details>
<summary><strong>이상 현상의 종류에 대해 설명해주세요.</strong></summary>  
<hr>
<ol>
  <li>삽입 이상 : 자료를 삽입할 때 특정 속성에 해당하는 값이 없어 NULL을 입력해야 하는 현상</li>
  <li>갱신 이상 : 중복된 데이터 중 일부만 수정되어 데이터 모순이 일어나는 현상</li>
  <li>삭제 이상 : 어떤 정보를 삭제하면, 의도하지 않은 다른 정보까지 삭제되어버리는 현상</li>
</ol>
<hr>
</details>


<details>
<summary><strong>SQL Injection이 무엇인지 설명해주세요.</strong></summary>  
<hr>
<ul>
  <li>공격자가 악의적인 의도를 갖는 SQL 구문을 삽입하여 데이터베이스를 비정상적으로 조작하는 코드 인젝션 공격 기법입니다.</li>
</ul>
<hr>
</details>


<details>
<summary><strong>SQL Injection을 방어하기 위한 방법에 대해 알고 있다면 설명해주세요.</strong></summary>  
<hr>
<ol>
  <li>입력값을 검증하여 사용자의 입력이 쿼리에 동적으로 영향을 주는 경우, 입력된 값이 개발자가 의도한 값(유효값) 인지 검증합니다.</li>
  <li>저장 프로시저를 사용합니다.
    <ul>
      <li>저장 프로시저란 사용하고자 하는 Query에 미리 형식을 지정하는 것을 말한다. 지정된 형식의 데이터가 아니면 Query가 실행되지 않기 때문에 보안성이 크게 향상한다.</li>
    </ul>
  </li>
</ol>
<hr>
</details>


<details>
<summary><strong>트랜잭션이 무엇인가?</strong></summary>  
<hr>
<ul>
  <li>작업들을 모두 처리하거나 처리하지 못할 경우 이전 상태로 복구하여 작업의 일부만 적용되는 현상이 발생하지 않게 만들어주는 기능입니다.</li>
  <li>하나의 트랜잭션은 Commit(작업완료)되거나 Rollback(취소)됩니다.</li>
</ul>
<hr>
</details>

<details>
<summary><strong>트랜잭션의 ACID란?</strong></summary>  
<hr>
<ol>
  <li>원자성(Atomicity) 작업이 모두 반영되던지 아니면 전혀 반영되지 않아야 한다.</li>
  <li>일관성(Consistency) 실행이 완료되면 언제나 일관성 있는 상태를 유지해야 한다.</li>
  <li>독립성(Isolation) 둘 이상 트랜잭션이 동시에 실행될 경우 서로의 연산에 끼어들 수 없다.</li>
  <li>영속성(Durability) 완료된 결과는 영구적으로 반영되어야 한다.</li>
</ol>
<hr>
</details>

<details>
<summary><strong>트랜잭션의 격리수준에 대해 설명해주세요.</strong></summary>  
<hr>
<ul>
  <li>동시에 여러 트랜잭션이 처리될 때, 특정 트랜잭션이 다른 트랜잭션에서 변경하거나 조회하는 데이터를 볼 수 있도록 허용할지 말지를 결정하는 것입니다.</li>
  <li>격리수준은 4가지로 정의 가능
    <ol>
      <li>READ UNCOMMITTED(커밋되지 않은 읽기)</li>
      <li>READ COMMITTED(커밋된 읽기)</li>
      <li>REPEATABLE READ(반복 가능한 읽기)</li>
      <li>SERIALIZABLE(직렬화 가능)</li>
      <li>순서대로 READ UNCOMMITTED의 격리 수준이 가장 낮고 SERIALIZABLE의 격리 수준이 가장 높습니다.</li>
    </ol>
  </li>
</ul>
<hr>
</details>


<details>
<summary><strong>트랜잭션이 필요한 이유는 무엇인가?</strong></summary>  
<hr>
<ul>
  <li>데이터의 일관성을 유지하면서 안정적으로 데이터를 복구하기 위함입니다.</li>
</ul>
<hr>
</details>


<details>
<summary><strong>관계형DB(RDBMS), 비관계형DB(Nosql)의 차이점이 무엇인가?</strong></summary>  
<hr>
<ul>
  <li>RDBMS는 다른 테이블들과 관계를 맺고 모여있는 집합체로, 테이블간 join이 가능합니다.</li>
  <li>Nosql은 테이블간 관계를 정의하지 않아, 테이블간 join이 불가능합니다.</li>
</ul>
<hr>
</details>


<details>
<summary><strong>JOIN 종류에 대해 설명해보세요</strong></summary>  
<hr>
<ul>
  <li>INNER JOIN : 두 테이블에서 같은 값만 가져옵니다.</li>
  <li>OUTER JOIN
    <ol>
      <li>LEFT JOIN : 왼쪽 테이블을 기준으로 오른쪽의 테이블을 매치합니다. 왼쪽은 무조건 표시하고, 매치되는 레코드가 없으면 NULL을 표시합니다.</li>
      <li>RIGHT JOIN : 오른쪽 테이블을 기준으로 왼쪽 테이블을 매치합니다. 오른쪽은 무조건 표시하고, 매치되는 레코드가 없으면 NULL을 표시합니다.</li>
    </ol>
  </li>
  <li>CROSS JOIN : 두 테이블의 모든 경우의 수를 결합합니다.</li>
</ul>
<hr>
</details>


<details>
<summary><strong>DB 인덱스가 무엇인가?</strong></summary>  
<hr>
<ul>
  <li>테이블을 처음부터 끝까지 검색하는 방법인 FTS(Full Table Scan)과는 달리 인덱스를 검색하여 해당 자료의 테이블을 엑세스 하는 방법입니다.</li>
</ul>
<hr>
</details>


<details>
<summary><strong>DB 인덱스를 사용하는 이유 및 장단점?</strong></summary>  
<hr>
<ul>
  <li>인덱스를 사용하는 이유
    <ol>
      <li>검색 성능을 향상시키기 위함입니다.</li>
      <li>테이블의 데이터는 순서 없이 쌓이게 되므로 특정 조건의 데이터를 찾으려면 테이블의 모든 데이터에 접근하여 비교하는 과정이 필요합니다.(full table scan) 하지만, 인덱스가 있는 경우 search-key가 정렬되어 있기 때문에 조건 검색 시 속도가 빠릅니다.</li>
    </ol>
  </li>
  <li>장점 : 테이블 조회 속도 향상</li>
  <li>단점
    <ol>
      <li>인덱스를 관리하기 위해 데이터베이스의 약 10%정도의 추가 저장공간이 필요</li>
      <li>인덱스를 잘못 관리하면 오히려 성능이 저하 (CREATE, DELETE, UPDATE가 빈번한 속성에 인덱스를 걸게 되면, 인덱스의 크기가 비대해져서 성능이 오히려 저하)</li>
    </ol>
  </li>
</ul>
<hr>
</details>


<details>
<summary><strong>DB 락의 종류는?</strong></summary>  
<hr>
<ul>
  <li>공유락(LS, Shared Lock) : Read Lock라고도 하는 공유락은 트랜잭션이 읽기를 할 때 사용하는 락이며, 데이터를 읽기만하기 때문에 같은 공유락 끼리는 동시에 접근이 가능합니다.</li>
  <li>베타락(LX, Exclusive Lock) : Write Lock라고도 하는 베타락은 데이터를 변경할 때 사용하는 락입니다. 트랜잭션이 완료될 때까지 유지되며, 베타락이 끝나기 전까지 어떠한 접근도 허용하지 않습니다.</li>
</ul>
<hr>
</details>


<details>
<summary><strong>Redis에 대해 간단히 설명해주세요.</strong></summary>  
<hr>
<ul>
  <li>Key, Value 구조의 비정형 데이터를 저장하고 관리하기 위한 오픈 소스 기반의 비관계형 데이터 베이스 관리 시스템 (DBMS)입니다.</li>
  <li>데이터베이스, 캐시, 메세지 브로커로 사용되며 인메모리 데이터 구조를 가진 저장소입니다.</li>
  <li>Redis의 특징
    <ul>
      <li>영속성을 지원하는 인메모리 데이터 저장소</li>
      <li>읽기 성능 증대를 위한 서버 측 복제를 지원</li>
      <li>쓰기 성능 증대를 위한 클라이언트 측 샤딩(Sharding) 지원</li>
      <li>다양한 서비스에서 사용되며 검증된 기술</li>
      <li>String, List, Hash, Set, Sorted Set과 같은 다양한 데이터형을 지원. 메모리 저장소임에도 불구하고 많은 데이터형을 지원하므로 다양한 기능을 구현</li>
    </ul>
  </li>
</ul>
<hr>
</details>


<details>
<summary><strong>Redis와 Memcached의 차이에 대해 간단히 설명해주세요.</strong></summary>  
<hr>
<ul>
  <li>데이터 타입 : Memcached 는 데이터를 문자열로만 저장하는 반면, Redis 는 조금 더 다양한 자료형을 지원</li>
  <li>데이터 지속성 : Memcached 에는 없지만 Redis 에는 특징 중 하나는 데이터 지속성 (Persistence)</li>
  <li>데이터 길이 : Redis 의 key 또는 string 은 512MB 에 달하는 크기를 가질 수 있는 반면 Memcached 의 key 는 250 바이트의 크기밖에 갖지 못한다.</li>
  <li>데이터 삭제 방법 : Memcached 나 Redis 나 모두 LRU (Least Recently Used) 방법을 통해 잔여 기간이 긴 데이터를 삭제한다. 그러나 Redis 는 No Eviction (데이터를 삭제하지 않고 메모리가 차면 key 추가를 허용하지 않음) 이나 TTL (Time to Live : TTL 표기가 된 데이터를 먼저 지우고 나머지는 아직 유효한 것으로 간주함) 등의 추가적인 방법을 통해서도 데이터를 관리할 수 있다. </li>
  <li>레플리카 : Redis 는 자체적으로 Replica 를 형성하여 두 개의 다른 서버에서도 동일한 데이터가 보관될 수 있도록 하지만, Memcached 는 외부 소프트웨어를 사용하지 않는 이상 Replica 를 제공하지 않는다. </li>
</ul>
<hr>
</details>


<details>
<summary><strong>Elastic Search에 대해 간단히 설명해주세요.</strong></summary>  
<hr>
<ul>
  <li>Elasticsearch는 Apache Lucene( 아파치 루씬 ) 기반의 Java 오픈소스 분산 검색 엔진입니다.</li>
  <li>방대한 양의 데이터를 신속하게, 거의 실시간(NRT, Near Real Time)으로 저장, 검색, 분석할 수 있습니다.</li>
  <li>Elasticsearch는 검색을 위해 단독으로 사용되기도 하며, ELK(Elasticsearch / Logstatsh / Kibana)스택으로 사용되기도 합니다.</li>
</ul>
<hr>
</details>


<details>
<summary><strong>Elastic Search의 키워드 검색과 RDMS의 LIKE 검색의 차이에 대해 간단히 설명해주세요.</strong></summary>  
<hr>
<ul>
  <li>RDBMS는 단순 텍스트매칭에 대한 검색만을 제공해 동의어나 유의어 같은 검색은 불가능합니다.</li>
  <li>Elastic Search는 동의어나 유의어를 활용한 검색이 가능하며, 비정형 데이터의 색인과 검색이 가능하고, 역색인 지원으로 매우 빠른 검색이 가능합니다.</li>
</ul>
<hr>
</details>


<details>
<summary><strong>데이터베이스 언어(DDL, DML, DCL)에 대해 설명해주세요.</strong></summary>  
<hr>
<ul><li>답변</li></ul>
<hr>
</details>


<details>
<summary><strong>트리거(Trigger)에 대해 설명해주세요.</strong></summary>  
<hr>
<ul><li>답변</li></ul>
<hr>
</details>


<details>
<summary><strong>옵티마이저(Optimizer)에 대해 설명해주세요.</strong></summary>  
<hr>
<ul><li>답변</li></ul>
<hr>
</details>



<details>
<summary><strong>DB 튜닝이 무엇인지 설명해주세요.</strong></summary>  
<hr>
<ul><li>답변</li></ul>
<hr>
</details>


<details>
<summary><strong>DB 튜닝의 3단계에 대해 설명해주세요.</strong></summary>  
<hr>
<ul><li>답변</li></ul>
<hr>
</details>


<details>
<summary><strong>group by 역할에 대해 설명해주세요</strong></summary>  
<hr>
<ul><li>답변</li></ul>
<hr>
</details>


<details>
<summary><strong>DELETE, TRUNCATE, DROP의 차이에 대해 설명해주세요</strong></summary>  
<hr>
<ul><li>답변</li></ul>
<hr>
</details>


<details>
<summary><strong>데이터베이스 클러스터링과 리플리케이션의 차이에 대해 설명해주세요</strong></summary>  
<hr>
<ul><li>답변</li></ul>
<hr>
</details>


<details>
<summary><strong>HAVING과 WHERE 차이에 대해 설명해주세요</strong></summary>  
<hr>
<ul><li>답변</li></ul>
<hr>
</details>


<details>
<summary><strong>JOIN에서 ON과 WHERE 차이에 대해 설명해주세요</strong></summary>  
<hr>
<ul><li>답변</li></ul>
<hr>
</details>

<details>
<summary><strong>데이터베이스의 특징에 대해 설명해주세요</strong></summary>  
<hr>
<ul><li>답변</li></ul>
<hr>
</details>

<details>
<summary><strong>쿼리의 수행 순서를 설명해주세요</strong></summary>  
<hr>
<ul><li>답변</li></ul>
<hr>
</details>

<details>
<summary><strong>inner join과 outer join의 차이를 설명해주세요</strong></summary>  
<hr>
<ul><li>답변</li></ul>
<hr>
</details>

<details>
<summary><strong>데이터베이스에서 다양한 유형의 관계에 대해 설명해주세요</strong></summary>  
<hr>
<ul><li>답변</li></ul>
<hr>
</details>

<details>
<summary><strong>데이터베이스 뷰에 대해 설명해주세요</strong></summary>  
<hr>
<ul><li>답변</li></ul>
<hr>
</details>

<details>
<summary><strong>데이터베이스 뷰의 장점과 단점을 설명해주세요</strong></summary>  
<hr>
<ul><li>답변</li></ul>
<hr>
</details>

<details>
<summary><strong>ER 모델에 대해 설명해주세요</strong></summary>  
<hr>
<ul><li>답변</li></ul>
<hr>
</details>

<details>
<summary><strong>기본 키(Primary key)와 복합 키(Compound key)에 대해 설명해주세요</strong></summary>  
<hr>
<ul><li>답변</li></ul>
<hr>
</details>

<details>
<summary><strong>트랜잭션 상태에 대해 설명해주세요</strong></summary>  
<hr>
<ul><li>답변</li></ul>
<hr>
</details>
