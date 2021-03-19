# code-with-quarkus-rivelazione project

This project uses Quarkus, the Supersonic Subatomic Java Framework.

If you want to learn more about Quarkus, please visit its website: https://quarkus.io/ .

## Running the application in dev mode

You can run your application in dev mode that enables live coding using:
```shell script
./mvnw compile quarkus:dev
```

> **_NOTE:_**  Quarkus now ships with a Dev UI, which is available in dev mode only at http://localhost:8080/q/dev/.

## Packaging and running the application

The application can be packaged using:
```shell script
./mvnw package
```
It produces the `quarkus-run.jar` file in the `target/quarkus-app/` directory.
Be aware that it’s not an _über-jar_ as the dependencies are copied into the `target/quarkus-app/lib/` directory.

If you want to build an _über-jar_, execute the following command:
```shell script
./mvnw package -Dquarkus.package.type=uber-jar
```

The application is now runnable using `java -jar target/quarkus-app/quarkus-run.jar`.

## Creating a native executable

You can create a native executable using: 
```shell script
./mvnw package -Pnative
```

Or, if you don't have GraalVM installed, you can run the native executable build in a container using: 
```shell script
./mvnw package -Pnative -Dquarkus.native.container-build=true
```

You can then execute your native executable with: `./target/code-with-quarkus-rivelazione-1.0.0-SNAPSHOT-runner`

If you want to learn more about building native executables, please consult https://quarkus.io/guides/maven-tooling.html.

## Related guides

- OptaPlanner AI constraint solver ([guide](https://quarkus.io/guides/optaplanner)): Optimize planning of vehicle routes, employee rosters, maintenance schedules, task assignments, school timetables, conference schedules, etc.
- Apache Kafka Client ([guide](https://quarkus.io/guides/kafka)): Connect to Apache Kafka with its native API
- Camel Avro ([guide](https://camel.apache.org/camel-quarkus/latest/reference/extensions/avro.html)): Serialize and deserialize messages using Apache Avro binary data format
- RESTEasy Multipart ([guide](https://quarkus.io/guides/rest-json#multipart-support)): Multipart support for RESTEasy
- Quarkus Extension for Spring Web API ([guide](https://quarkus.io/guides/spring-web)): Use Spring Web annotations to create your REST services
- RESTEasy JAX-RS ([guide](https://quarkus.io/guides/rest-json)): REST endpoint framework implementing JAX-RS and more
- SmallRye JWT ([guide](https://quarkus.io/guides/security-jwt)): Secure your applications with JSON Web Token
- Logging JSON ([guide](https://quarkus.io/guides/logging#json-logging)): Add JSON formatter for console logging
- Kubernetes ([guide](https://quarkus.io/guides/kubernetes)): Generate Kubernetes resources from annotations
- SmallRye Metrics ([guide](https://quarkus.io/guides/microprofile-metrics)): Expose metrics for your services
- MongoDB client ([guide](https://quarkus.io/guides/mongodb)): Connect to MongoDB in either imperative or reactive style
- Camel MongoDB ([guide](https://camel.apache.org/camel-quarkus/latest/reference/extensions/mongodb.html)): Perform operations on MongoDB documents and collections
- Camel Timer ([guide](https://camel.apache.org/camel-quarkus/latest/reference/extensions/timer.html)): Generate messages in specified intervals using java.util.Timer
- Reactive Routes ([guide](https://quarkus.io/guides/reactive-routes)): REST framework offering the route model to define non blocking endpoints
- OpenID Connect ([guide](https://quarkus.io/guides/security-openid-connect)): Secure your applications with OpenID Connect Adapter and IDP such as Keycloak
- Apache Kafka Streams ([guide](https://quarkus.io/guides/kafka-streams)): Implement stream processing applications based on Apache Kafka
- Camel MongoDB GridFS ([guide](https://camel.apache.org/camel-quarkus/latest/reference/extensions/mongodb-gridfs.html)): Interact with MongoDB GridFS

## Provided examples

### Logging JSON example

This example let you go faster with your jet aircraft, your speed is logged when you send a new request.<br/> When you reach the speed of sound, a "Sonic Boom" error is going to be thrown and logged. Boom!

[Related guide section...](https://quarkus.io/guides/logging#configuration)

### RESTEasy JAX-RS example

REST is easy peasy with this Hello World RESTEasy resource.

[Related guide section...](https://quarkus.io/guides/getting-started#the-jax-rs-resources)

### Spring Web example

Spring, the Quarkus way! A Hello World Spring Web Controller.

[Related guide section...](https://quarkus.io/guides/spring-web#greetingcontroller)
