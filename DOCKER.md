# First Responder Demo

First, build the WAR file:

```shell
mvn clean package
```

Then build a Docker image for the deployed WAR

```shell
docker build -t first_responder_demo -f src/main/docker/wildfly/Dockerfile .
```


