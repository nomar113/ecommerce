## Curso de Kafka da Alura: 
# Kafka: produtores, consumidores e streams

1. Baixar o kafka no site, descompactar em alguma pasta:
2. Iniciar o zookeper:
```sh
bin/zookeeper-server-start.sh config/zookeeper.properties
```
3. Iniciar o Kafka:
```sh
bin/kafka-server-start.sh config/server.properties
```

## Comandos do Kafka:
### descrever os tópicos:
```sh
bin/kafka-topics.sh --bootstrap-server localhost:9092 --describe
```

### produzir uma mensagem
```sh
bin/kafka-console-producer.sh --bootstrap-server localhost:9092 --topic ECOMMERCE_NEW_ORDER
```

### consumir uma mensagem
```sh
bin/kafka-console-consumer.sh --bootstrap-server localhost:9092 --topic ECOMMERCE_NEW_ORDER
```

### alterar as partições de um tópico:
```sh
bin/kafka-topics.sh --alter --bootstrap-server localhost:9092 --topic ECOMMERCE_NEW_ORDER --partitions 3
```

### analisar os grupos de consumers:
```sh
bin/kafka-consumer-groups.sh --bootstrap-server localhost:9092 --describe --all-groups
```
