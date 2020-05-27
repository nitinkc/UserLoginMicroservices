# UserLoginMicroservices




## Spring cloud Bus - Dynamic Configuration Updates

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

## Logstash
