# kafka_streaming


1. Creating the multi container environment: `docker-compose up -d` 
2. Shows detials of the above: `docker-compose ps `
3. Creating a topic with set partitions and replicas: `docker exec -it kafka1 kafka-topics.sh --create --topic test-topic --partitions  3 --replication-factor 2 --bootstrap-server kafka1:9092`

4. Describing a topic: `docker exec -it kafka1 kafka-topics.sh  --bootstrap-server localhost:9092 --describe --topic test-topic`
5. Altering a topic to have more partitions: `kafka1 kafka-topics.sh --bootstrap-server localhost:9092 --alter  --topic test-topic` --partitions 3
6. Stopping a kafka container: `docker stop {container_name}`. Eg: docker stop kafka1