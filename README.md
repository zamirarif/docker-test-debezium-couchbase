# docker-test-debezium-couchbase
### A docker file to setup debezium for mysql and couchbase sink connector

### How to use it

```
 C:\Users\zamir.arif\debizium>docker-compose up -d --build
```
```
 C:\Users\zamir.arif\debizium>docker-compose ps
The system cannot find the path specified.
     Name                    Command               State                                                                                                                  Ports                      
-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
appserver         tail -F anything                 Up      0.0.0.0:38080->38080/tcp, 0.0.0.0:48080->48080/tcp                                                                                        
broker            /etc/confluent/docker/run        Up      0.0.0.0:29092->29092/tcp, 0.0.0.0:9092->9092/tcp                                                                                          
connect           bash -c if [ ! -d /usr/sha ...   Up      0.0.0.0:8083->8083/tcp, 9092/tcp                                                                                                          
control-center    /etc/confluent/docker/run        Up      0.0.0.0:9021->9021/tcp                                                                                                                    
couchbase         /entrypoint.sh couchbase-s ...   Up      11207/tcp, 0.0.0.0:11210->11210/tcp, 11211/tcp, 18091/tcp, 18092/tcp, 18093/tcp, 18094/tcp, 18095/tcp, 18096/tcp, 0.0.0.0:8091->8091/tcp, 0.0.0.0:8092->8092/tcp, 0.0.0.0:8093->8093/tcp, 0.0.0.0:8094->8094/tcp, 8095/tcp, 8096/tcp
ksql-cli          /bin/sh                          Up                                                                                                                                                
ksql-datagen      bash -c echo Waiting for K ...   Up                                                                                                                                                
ksql-server       /etc/confluent/docker/run        Up      0.0.0.0:8088->8088/tcp                                                                                                                    
mysql             docker-entrypoint.sh mysqld      Up      0.0.0.0:8080->28080/tcp, 0.0.0.0:3306->3306/tcp, 33060/tcp                                                                                
rest-proxy        /etc/confluent/docker/run        Up      0.0.0.0:8082->8082/tcp                                                                                                                    
schema-registry   /etc/confluent/docker/run        Up      0.0.0.0:8081->8081/tcp                                                                                                                    
zookeeper         /etc/confluent/docker/run        Up      0.0.0.0:2181->2181/tcp, 2888/tcp, 3888/tcp 
```
makes sure all the containers are up and running.

