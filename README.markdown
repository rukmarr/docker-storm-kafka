## Usage
This module contains example topology demonstrating storm-kafka-client spout. Please ensure you have a Kafka instance running at localhost:9092 before you deploy the topologies.

The module is built by running `mvn clean package -Dstorm.kafka.client.version=<kafka_broker_version>`, where the property should match the Kafka version you want to use. For example, for Kafka 0.11.0.0 the `<kafka_broker_version>` would be `0.11.0.0`. This will generate the `target/storm-kafka-client-examples-VERSION.jar` file. The jar contains all dependencies and can be submitted to Storm via the Storm CLI, e.g.
```
storm jar storm-kafka-client-examples-2.0.0-SNAPSHOT.jar org.apache.storm.kafka.spout.KafkaSpoutStormBoltTopology
```
will submit the topologies set up by KafkaSpoutStormBoltTopology to Storm.

Note that this example produces a jar containing all dependencies for ease of use.