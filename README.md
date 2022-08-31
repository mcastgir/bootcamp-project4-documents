# Documents
> **Documents** Bootcamp NTT Data

This project include:
- Project Architecture Microservices
- Databases exported Json
- Model Databases
- Json exported Postman

## General Configuration in Docker

---

### Microservices

1. Create Image Config Server in Docker
```  
docker build -t microservice-name .
```

2. Create Container

```
docker run -p 8080:8080 --name microservice-name --link mongo-instance:latest -d microservice-name:latest
```

---

### Mongo

1. Create Image Config Server in Docker
```  
docker pull mongo:latest
```

2. Create Container

```
docker run -d -p 27017:27017 --name mongo-instance mongo:latest
```

3. Show databases Command Line in MongoDB

```
show databases
use <database>
show collections
db.<table>.find()
db.<table>.find().pretty()
```

---

### SonarQube

1. Create Image Config Server in Docker
```  
docker pull sonarqube
```

2. Create Container

```
docker run -d --name sonarqube -p 9001:9000 -p 9093:9093 sonarqube
```

---

### Kafka and zookeeper

1. Run docker-compose
```  
run docker-compose
```

2. List Topics in kafka

```
kafka-topics.sh --list --bootstrap-server localhost:9093
```

3. Create Topics in kafka

```
kafka-topics.sh --create --topic topic-person --bootstrap-server localhost:9092 --replication-factor 1 --partitions 1
```

---

### Redis

1. Create Image Config Server in Docker
```  
docker pull redis
```

2. Create Container

```
docker run --name redis-instance -p 6379:6379 -d redis:latest
```

---

### Redis

1. Create Image Config Server in Docker
```  
docker pull mysql
```

2. Create Container

```
docker run --name mysql-instance -e MYSQL_ROOT_PASSWORD=admin123 -p 3306:3306 -d mysql:latest
```