# My Code for Udemy course by Sean Campbell [Java Microservices: CQRS & Event Sourcing with Kafka](https://www.udemy.com/course/java-microservices-cqrs-event-sourcing-with-kafka/)

Learn how to create microservices that are based on CQRS & Event Sourcing. Powered by Spring Boot and Apache Kafka.

## Setup

- Java 11 (Java 16 in the course)
- Maven 
- Docker
- Docker Compose
- wip...

## 

```bash
docker network create --attachable -d bridge techbankNet
docker run -it -d --name mongo-container -p 27017:27017 --network techbankNet --restart always -v mongodb_data_container:/data/db mongo:4.4.14
docker run -it -d --name mysql-container -p 13306:3306 --network techbankNet -e MYSQL_ROOT_PASSWORD=techbankRootPsw --restart always -v mysql_data_container:/var/lib/mysql mysql:8.0.29
docker run -it -d --name adminer -p 18080:8080 --network techbankNet -e ADMINER_DEFAULT_SERVER=mysql-container --restart always adminer:4.8.1
cd docker-compose/kafka-dc
docker-compose up -d
```
