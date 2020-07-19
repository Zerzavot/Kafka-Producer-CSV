# Kafka-Producer-CSV

We are gonna make a kafka producer and send them to kafka console consumer. Then, we send them to a csv file</br> You can find the file *results.csv* in your kafka file.

- [x] Download Kafka and Zookeeper 
- [ ] Start Zookeeper
- [ ] Start Kafka
- [ ] Create a topic
- [ ] Run Kafka-Console-Consumer
- [ ] Writing output on a CSV file

### Start the Zookeeper

```
ubuntu@ubuntu-pc:~/kafka_2.12-2.0.0$ bin/zookeeper-server-start.sh config/zookeeper.properties 

```
![Ekran Görüntüsü - 2020-07-19 14-13-16](https://user-images.githubusercontent.com/50207648/87873404-2a641400-c9ca-11ea-8224-67fe72a252b9.png)

### Start the Kafka server

```
ubuntu@ubuntu-pc:~/kafka_2.12-2.0.0$ kafka-server-start.sh config/server.properties

```
![Ekran Görüntüsü - 2020-07-19 14-08-34](https://user-images.githubusercontent.com/50207648/87873394-1fa97f00-c9ca-11ea-8cad-dea75faa0fc8.png)

### Create a topic
```
ubuntu@ubuntu-pc:~/kafka_2.12-2.0.0$ kafka-server-start.sh config/server.properties
ubuntu@ubuntu-pc:~/kafka_2.12-2.0.0$ bin/kafka-topics.sh --create --zookeeper localhost:2181 --replication-factor 1 --partitions 1 --topic test
Created topic "test".

```

![Ekran Görüntüsü - 2020-07-19 14-24-00](https://user-images.githubusercontent.com/50207648/87873589-8da27600-c9cb-11ea-831b-84254b956515.png)

### Run Kafka-console-consumer
```
ubuntu@ubuntu-pc:~/kafka_2.12-2.0.0$ kafka-console-consumer.sh --bootstrap-server localhost:9092 --topic topicNew1

```
![Ekran Görüntüsü - 2020-07-19 14-36-39](https://user-images.githubusercontent.com/50207648/87873835-6c428980-c9cd-11ea-992e-352a5706f855.png)

### Writing on a CSV file

```
ubuntu@ubuntu-pc:~/kafka_2.12-2.0.0$ kafka-console-consumer.sh --bootstrap-server localhost:9092 --topic topicNew1 > results.csv
```
![Ekran Görüntüsü - 2020-07-19 14-42-14](https://user-images.githubusercontent.com/50207648/87873912-11f5f880-c9ce-11ea-87a6-1fa95dc8bdef.png)

