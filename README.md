# Kafka PoC w/ NodeJS Producers and Consumers using Docker

## serve the containers

docker-compose up -d

## exec inside kafka container

docker exec -it kafka /bin/sh

## change dir to kafka bin to create new topic

cd /opt/kafka_2.13-2.8.1/bin

## exec below where topic_name is your topic name, change partitions as necessary

kafka-topics.sh --create --zookeeper zookeeper:2181 --replication-factor 1 --partitions 1 --topic topic_name

## list topics

kafka-topics.sh --list --zookeeper zookeeper:2181

## install packages

npm i

## run the code

npm run start
