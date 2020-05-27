# UserLoginMicroservices


## Rabbit MQ

On Mac

⇒  brew services start/stop rabbitmq

## Spring cloud Bus - Dynamic Configuration Updates (Needs Rabbit MQ)

Modify the properties and commit the changes to the centralized config repo.

Execute the following: Spring Cloud Config server

http://localhost:9999/actuator/bus-refresh

Re-test to check the modified property value.


## Zipkin Tracing server

https://zipkin.io/pages/quickstart

Start Using Java8

```sh
curl -sSL https://zipkin.io/quickstart.sh | bash -s
java -jar zipkin.jar
```

Access the server on the loalhost at : http://localhost:9411/zipkin/

#### Enable Zipkin Tracing (on a particular microservice)

Zipkin allows a tracing id to each call.

```sh
spring.zipkin.base-url=http://localhost:9411
spring.zipkin.sender.type=web
spring.sleuth.sampler.probability=1
```

## Enable Logging

Give an absolute path. Below example creates the file in the root directory.

```sh
logging.file.name=users-ws.log
```

## Elasticsearch

Download and unzip from https://www.elastic.co/downloads/elasticsearch

cd into the directory and run bin/elasticsearch

runs on default port 9200

http://localhost:9200/

## Logstash

Download and Unzip the Logstash zip. https://www.elastic.co/downloads/logstash

create a .conf file

cd into the unzipped directory and execute 

bin/logstash -f nitin-config.conf

## Kibana

To Visualize the search logs properly, download Kibana

https://www.elastic.co/downloads/kibana

cd into the directory

config Kibana via kibana.yml to have elasticsearch.host. By default it runs for port 9200 for Elasticsearch

execute bin/kibana
