# kafka-zookeeper
helm create kafka-zookeeper
Update or add the yaml files accordingly 
helm install my-kafka-zookeeper ./kafka-zookeeper
helm package kafka-zookeeper

Command to check the deployment
kubectl get all

Check the kafka and zookeeper
kubectl exec -it kafka-0 -- /bin/bash
kafka-topics.sh --list --bootstrap-server localhost:9092

To produce any message in the test topic 
kafka-console-producer.sh --broker-list 130.211.195.144:30092 --topic test

To check the test topic 
kafka-console-consumer.sh --bootstrap-server 130.211.195.144:30092 --topic test --from-beginning

kubectl exec -it zookeeper-0 -- /bin/bash

zkCli.sh -server localhost:2181

zkCli.sh -server 35.188.127.151:2181

