# kafka
Download binary file from Apache kafka. Donot download src file. Download file from https://kafka.apache.org/downloads

# kafka-publisher
Apache Kafka Publisher Example using SpringBoot. Go to D:\kafka\kafka_2.13-2.8.1\bin\windows and open the command prompt from this path then run the below command.

# start zookeeper.start bat file like below
zookeeper-server-start.bat D:\kafka\kafka_2.13-2.8.1\config\zookeeper.properties

# start kafka server
kafka-server-start.bat D:\kafka\kafka_2.13-2.8.1\config\server.properties

# Create Topic:
kafka-topics.bat --create --zookeeper localhost:2181 --replication-factor 1 --partitions 1 -topic kafkaTopic

# List All Topic
kafka-topics.bat --list --zookeeper localhost:2181

# Produce a message 
kafka-console-producer.bat --broker-list localhost:9092 --topic kafkaTopic

# Consume a message
kafka-console-consumer.bat --bootstrap-server localhost:9092 --topic kafkaTopic
