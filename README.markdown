### Запуск кластера
```
	docker-compose up -d
```

### Запуск топологии:

```
  docker-compose exec topology sh
  > storm jar target/storm-kafka-client-examples-2.2.0.jar org.apache.storm.kafka.spout.KafkaSpoutStormBoltTopology
```

### Запуск продьюсера:

```
  docker-compose exec kafka sh
  > kafka-console-producer.sh --topic wordCount-topic --bootstrap-server localhost:9092
```


