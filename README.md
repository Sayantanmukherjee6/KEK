# KEK

* To start Kafka-ElasticSearch-Kibana with Kafka-Connector run: 
	* <b> docker-compose -f docker-compose-KEK.yaml up -d </b>

### <u>Example: Logging system using KEK</u> 
* Start Fluentd agent (<b>td-agent.conf</b> provided in this repo). Other log collection framework can also be used.
* Start docker-compose-KEK.yaml. 
* Change <b>/etc/hosts</b>:

 	* ![Image of /etc/hosts/](https://miro.medium.com/max/198/1*0GdRZygt5BzxZq17adpunA.png)   
 
 * Create the Kafka-Connector by using Kafka-Connect API (An sample JSON is provided : <b>connector.json</b>).
 * Dump system/code logs in <b> /tmp/logs/</b>  directory.
 * Open Kibana (<b>http://localhost:5601</b>) and configure index pattern for the current topic. After it is configured properly, in the Discover tab of Kibana the logs will be displayed.

### <u>Installing and Configuring Fluentd</u>
* https://docs.fluentd.org/installation/install-by-deb
* td-agent.conf is located at <b>/etc/td-agent.conf</b>
* After modification of td-agent.conf file run <b> sudo service td-agent restart.</b>

### <u>Sources</u>

* https://medium.com/@raymasson/kafka-elasticsearch-connector-fa92a8e3b0bc
* https://www.cloudboxlabs.com/blog/distributed-log-analytics-using-apache-kafka-kafka-connect-and-fluentd
* https://blog.treasuredata.com/blog/2015/07/07/collecting-docker-logs-with-fluentd/

 
