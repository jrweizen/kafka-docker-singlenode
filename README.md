# kafka-docker-singlenode

# https://towardsdatascience.com/getting-started-with-apache-kafka-in-python-604b3250aa05

# cria topico no kafka
kafka-topics --create --zookeeper localhost:32181 --replication-factor 1 --partitions 1 --topic twittertopic

# Describe topico criado no zookeeper
kafka-topics --describe --topic twittertopic --zookeeper 'localhost:32181'

# Sending messages - Producers(apps) needs to produce stuff
kafka-console-producer --broker-list localhost:29092 --topic twittertopic

# Consuming messages
kafka-console-consumer --bootstrap-server localhost:29092 --topic twittertopic --from-beginning
