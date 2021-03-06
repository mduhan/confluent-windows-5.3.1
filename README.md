Confluent
---------

Confluent offers a real-time data platform built around Apache Kafka.

Apache Kafka, an open source technology created by the founders of Confluent,
acts as a real-time, fault tolerant, highly scalable messaging system. It is
widely adopted for use cases ranging from collecting user activity data, logs,
application metrics, stock ticker data, and device instrumentation. Its key
strength is its ability to make high volume data available as a real-time stream
for consumption in systems with very different requirements—from batch systems
like Hadoop, to realtime systems that require low-latency access, to stream
processing engines that transform the data streams as they arrive.

This infrastructure lets you build around a single central nervous system
transmitting messages to all the different systems and applications within your
company.

# This is window supported patch of confluent 5.3.1.

## Cloning the confluent

First obtain the code by cloning the Git repository:

- $ git clone https://github.com/mduhan/confluent-windows-5.0.1.git
- $ cd confluent-windows-5.3.1


## Running Confluent in single command

- cd confluent-windows-5.3.1/bin/windows
- confluent.bat

## Running Confluent services separately

- cd confluent-windows-5.3.1/bin/windows
- zookeeper-start.bat
- kafka-start.bat
- schema-registry-start.bat
- worker-start.bat

### Services started :->

- zookeeper
- kafka
- schema-registry
- worker

## Access Worker
  
  http://localhost:8083/connectors

## Stopping Confluent

- cd confluent-windows-5.3.1/bin/windows
- confluent-stop.bat

## Reset Confluent ( This will delete complete data from zookeeper and kafka )

- cd confluent-windows-5.3.1/bin/windows
- confluent-reset.bat

## Start Console Consumer
- cd confluent-windows-5.3.1/bin/windows
- kafka-console-consumer.bat \ --bootstrap-server localhost:9092 --topic test

## Start Console Producer

- cd confluent-windows-5.3.1/bin/windows
- kafka-console-producer.bat \ --broker-list localhost:9092 --topic test --property "parse.key=true" --property "key.separator=:"

## Producer sample data to kafka
- 1:{"this is first message"}
- 2:{"this is second message"}
- 3:{"this is third message"}




