## 물리적 레이아웃

엘라스틱서치의 물리적 레이아웃에 해당하는 샤드(Shard)와 노드(node)를 반드시 이해하고 넘어 가야한다. 이유는 실제 엘라스틱서치를 이용하여 빅데이터 처리, 검색 시스템을 운영하면서 엘라스틱서치 서버 확장이 필요한 시기가 올 수 있기 때문이다.


### 노드 (Node)
간단히 말하면 노드는 엘라스틱서치를 실행하는 프로세스라고 말할 수 있으며, n개의 샤드로 구성된다. 하나의 서버 내부에서 엘라스틱서치를 여러번 실행하면 하나의 서버안에 n개의 노드를 가질 수 있다. 만약 또 다른 서버에 엘라스틱서치를 실행 했다면 그 또한 노드가 생성되는 것이고 n개의 노드들을 하나로 묶기위해서는 클러스터(Cluster)를 이용한다.

클러스터로 묶인 노드들은 각자의 역할을 수행을 할 수 있다. 각 노드에게 역할을 주기위해서는 config/elasticsearch.yml 에서 간단하게 수정이 가능하다.

#### 노드의 역할
데이타 노드 (Data node)
비데이터 노드 (Non-Data node)
클라이언트 노드 (Client node)

### 클러스터 (Cluster)
클러스터는 노드의 모임, 엘라스틱서치의 모임이라는 생각일 가지고 접근한다면 좀더 이해하기 쉬운것 같다. 각 노드들은 데이터를 나눠 저장하고 있으며 해당 노드들을 하나로 묶어 주는 개념이다.

### 샤드(Shard) / 리플리카(Replica)

클러스터를 설정하는 방법은 매우 간단하며 아래에서 elasticsearch.yml의 간단한 설정방법을 통해 알아보도록 하자.







## 참고 자료
[Elasticsearch in Action - understanding the logical layout documents, type, index](https://weng.gitbooks.io/elasticsearch-in-action/content/chapter2_diving_into_the_functionality/21understanding_the_logical_layout_documents_,type.html)

