>Udacity Data Streaming: 
1) OPT: 
``` 
List all topics
/usr/bin/kafka-topics --list --zookeeper localhost:2181

/usr/bin/kafka-console-consumer --bootstrap-server localhost:9092 --partition 0 --topic org.chicago.stations --from-beginning
org.chicago.cta.station.arrivals
org.chicago.cta.weather.v1
org.chicago.stations

/usr/bin/kafka-console-consumer --bootstrap-server localhost:9092 --partition 0 --topic org.chicago.cta.weather.v1 --from-beginning

Show content in the topic
/usr/bin/kafka-console-consumer --bootstrap-server localhost:9092 --partition 0 --topic org.chicago.cta.stations.table.v1 --from-beginning

Weather.rest_proxy_url}/topics/weather

Running the Simulation
1. cd producers
2. python simulation.py

To run the Faust Stream Processing Application:
1. cd consumers
2. faust -A faust_stream worker -l info

To run the KSQL Creation Script:
1. cd consumers
2. python ksql.py

To run the consumer: (NOTE: Do not run the consumer until you have reached Step 6!)
1. cd consumers
2. python server.py

``` 
2) SF Crime: 

``` 
1./usr/bin/zookeeper-server-start config/zookeeper.properties
2./usr/bin/kafka-server-start config/server.properties
3.python kafka_server.py
4.kafka-console-consumer --bootstrap-server localhost:9092 --topic com.udacity.project.sfcrimes --from-beginning

/usr/bin/kafka-console-consumer --bootstrap-server localhost:9092 --topic org.chicago.cta.stations.table.v1 --from-beginning

root@7aafb549a58e:/home/workspace/consumers# kill -15 1625
root@7aafb549a58e:/home/workspace/consumers# pgrep -lf python
``` 
