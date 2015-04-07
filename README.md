# dockerkafka_cmd
images for standard kafka tools(create topics, producer, consumer) from kafka software package


Run the tools as described in the kafka's document.
But these tools will run in the docker's container.

For example:

- List topics: `docker run --rm  duffqiu/kafka_cmd  "bin/kafka-topics.sh --list --zookeeper <docker host's ip>:2181"`

- Start producer: `docker run -it --rm duffqiu/kafka_cmd "bin/kafka-console-producer.sh --broker-list <docker host's ip>:9092 --topic <topic name>"`

   - note: the ip use in the container must be accessed by this container inside
   - note: for the tools need to input text, must use the -i -t parameter when run the container
