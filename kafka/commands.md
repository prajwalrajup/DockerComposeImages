# To Run it

```
docker-compose up -d
```

# To attach terminal

```
docker exec -it kafka bash
```

# Version of Kafka

```
kafka-broker-api-versions --bootstrap-server localhost:9092 --version
```

# Kafka consumer


### consumer message from beginning
```
kafka-console-consumer.sh --bootstrap-server dp-ev-kfk1.stage-ola-aws.olacabs.net:9092 --topic oms.gcs.outbound --group oms.gcs.outbound --from-beginning
```

### create group
```
kafka-consumer-groups.sh --bootstrap-server dp-ev-kfk1.stage-ola-aws.olacabs.net:9092 --describe --group <newGroup>
```

### list all consumers
```
kafka-consumer-groups.sh --bootstrap-server dp-ev-kfk1.stage-ola-aws.olacabs.net:9092 --list
```

# Topic


### new topic
```
kafka-topics.sh --bootstrap-server dp-ev-kfk1.stage-ola-azure.az.olacabs.net:9092 --create --topic <myNewTopic> --partitions 1 --replication-factor 1
```

### list all topics
```
kafka-topics.sh --bootstrap-server dp-ev-kfk1.stage-ola-azure.az.olacabs.net:9092 --list
```


### describe a topic
```
kafka-topics.sh --bootstrap-server dp-ev-kfk1.stage-ola-azure.az.olacabs.net:9092 --describe --topic <topicName>
```

### delete topic
```
kafka-topics.sh --zookeeper dp-ev-kfk1.stage-ola-azure.az.olacabs.net:9092 --delete --topic <topicName>
```

# Kafka producer

### create producer
```
kafka-console-producer.sh --bootstrap-server dp-ev-kfk1.stage-ola-aws.olacabs.net:9092 --topic <topicName>
```