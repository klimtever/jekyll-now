---
sort: 1
---

# Kafka Basics

In case of source 4, target 4 = 24 integration 


## Kafka Theory

### Topics
* a particular stream of data
* similar to a table in a database
* identified by its **name**
* split in **partitions**
    * each partion is ordered
    * each message within a partion gets an incremantal id, called **offset**

 Topic has 3 partitions (0, 1, 2), for exmaple.


### Broker

* Kafka cluster is composed of multiple brokers (servers)
* Identifed with its ID (integer)
* Each broker contains certain topic partitions  
  (has some data not whole data)
* Good number to get started is 3 broker, bt some big clusters have over 100 brokers

### Brokers & Topics
* Broker 101, 102, 103
* Topic_A with 2 partitions
* Topic_B with 3 partitions

### Topic Replication Factor 

In Sync Replica

### Producer
* Writes data to topics
* Automacally knows to which broker and partition to write to
    * acks=0: P will not wait for ack
    * acks = 1: P will wait for leader ack (limited data loss)
    * acks=all: leader + replicas acknowledgement (no data less)

### Message keys
* 

### Consumers
* Reads data from a topic 
* Data isread in order **within each partitions** 

### Consumers Groups 

### Consumer Offsets
* Kafa stores the offsets at which a consumer group has been reading, like bookmarking.
* sdd

### Delivery Semantics from Consumers
* At most once
* At least once (usually preferred)
* Exactly once

### Kafka Broker Discovery
Only need to connect on broker


### Zookeeper
* manages brokers
* helps in performing leader election for partitions
* Sends notifications to Kafka 
* Kafka can't work without Zookeeper

## Installation


```plantuml
@startuml component
actor client
node app
database db

db -> app
app -> c lient
@enduml
```



first_topic
bash-4.4# ./kafka-topics.sh --zookeeper zookeeper:2181 --topic first_topic first_topic --describe
Topic: first_topic	PartitionCount: 3	ReplicationFactor: 1	Configs:
	Topic: first_topic	Partition: 0	Leader: 1001	Replicas: 1001	Isr: 1001
	Topic: first_topic	Partition: 1	Leader: 1001	Replicas: 1001	Isr: 1001
	Topic: first_topic	Partition: 2	Leader: 1001	Replicas: 1001	Isr: 1001
bash-4.4# ./kafka-topics.sh --zookeeper zookeeper:2181 --topic second_topic --create --partitions 6 --replication-factor 1
WARNING: Due to limitations in metric names, topics with a period ('.') or underscore ('_') could collide. To avoid issues it is best to use either, but not both.
Created topic second_topic.

bash-4.4# ./kafka-topics.sh --zookeeper zookeeper:2181 --list
first_topic
bash-4.4# ./kafka-topics.sh --zookeeper 172.20.0.2:2181 --list
first_topic
bash-4.4# ./kafka-topics.sh --zookeeper zookeeper:2181 --topic first_topic first_topic --describe
Topic: first_topic	PartitionCount: 3	ReplicationFactor: 1	Configs:
	Topic: first_topic	Partition: 0	Leader: 1001	Replicas: 1001	Isr: 1001
	Topic: first_topic	Partition: 1	Leader: 1001	Replicas: 1001	Isr: 1001
	Topic: first_topic	Partition: 2	Leader: 1001	Replicas: 1001	Isr: 1001
bash-4.4# ./kafka-topics.sh --zookeeper zookeeper:2181 --topic second_topic --create --partitions 6 --replication-factor 1
WARNING: Due to limitations in metric names, topics with a period ('.') or underscore ('_') could collide. To avoid issues it is best to use either, but not both.
Created topic second_topic.