# Kafka Docker
Resources to use Kafka in Docker Containers

This repository includes Docker Compose files to startup Kafka environments with multiple brokers and clusters. Compose files were adapted to be interchangable with Confluent and Wurstmeister Kafka images and with configurations to allow container access from Docker host.

### Docker images
- **Kafka:**
- wurstmeister/kafka:2.12-2.1.0 (Scale version 2.12, Kafka version 2.1.0, https://hub.docker.com/r/wurstmeister/kafka/) 
- confluentinc/cp-kafka:5.1.0 (Confluent Platform 5.1.0, Kafka version 2.1.0)
- **Zookeeper:**
- zookeeper:3.5
- **Other Kafka Tools:**
- sheepkiller/kafka-manager

## Setup instructions

Kafka Cluster with one Kafka broker
```
docker-compose up
```

Kafka Cluster with three brokers
```
docker-compose -f multibroker.wurstmeister up
```

Two Kafka Clusters with three brokers each
```
docker-compose -f multicluster.wurstmeister up
```