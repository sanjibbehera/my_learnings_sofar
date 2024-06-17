## What is Kafka?
Apache Kafka is an open-source distributed event streaming platform used by thousands of companies for high-performance data pipelines, streaming analytics, data integration, and mission-critical applications.

## Publish-subscribe model
![Alt text](../Images/publish-subscribe-msg-flow.png?raw=true "Title")  

## Event Streaming
Event streaming is an implementation of the publish-subscribe messaging pattern with added capabilities.  
In event streaming, an event (also called a message or record) is simply a record of a state change in the system.  
An event stream is a sequence of events where events flow from publishers to subscribers.

## Consumer Group
Producers are applications you write that put data into topics and consumers are applications that read data from topics.  
If you're limited to a single consumer, your application might not catch up with all of the messages streaming in from a topic partition. By pulling multiple consumers together in a consumer group, however, Kafka allows for multiple consumers to read from multiple topic partitions, increasing messaging throughput.  
In a consumer group, multiple consumers read from the same topic, but each consumer reads from exclusive partitions.  

![Alt text](../Images/consumergroup.png?raw=true "Title")  


## Kafka clusters and Kafka brokers
A Kafka broker arranges transactions between producers and consumers. Brokers handle all requests from clients to write and read events.  
A Kafka cluster is simply a collection of one or more Kafka brokers.

## Kafka Architecture