## kafka listener 설정
KAFKA_ZOOKEEKER_CONNECT: zookeeper 주소 설정
KAFKA_ADVERTISED_LISTENERS: kafka producer, consumer에 할당되는 주소. client에서 활용.


## kafka-topics 명령
kafka kafka-topics

- --kafka-topics: Kafka 토픽 명령 실행

### kafka topic 생성
$ kafka kafka-topics --create --topic event-topic --bootstrap-server kafka:2102 --replication-factor 1 --partitions 1


- --create: 토픽 생성
- --topic [name]: [name]이란 이름으로 토픽 생성
- --bootstrap-server: kafka Broker Service. service:port로 액세스 가능
- --replication-factor 1: 래플리케이션 개수 지정
- --partition: 토픽 안에서 파티션 개수 설정


### kafka topic 확인
$ kafka kafka-topics --describe --topic event-topic --bootstrap-server kafka:2102

- --describe: 토픽 상세 설명 확인


### kafka producer 확인
kafka-console-producer --topic event-topic --broker-list kafka:2102


### kafka consumer 확인
kafka-console-consumer ---topic event-topic -bootstrap-server localhost:2102 --from-beginning