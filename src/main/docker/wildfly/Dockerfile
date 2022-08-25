FROM quay.io/wildfly/wildfly:26.1.1.Final-2
USER root
RUN mkdir /app
COPY first-responder-demo.war  /app
COPY opentelemetry-javaagent.jar  /app
WORKDIR /app
CMD ["java", "-javaagent:opentelemetry-javaagent.jar", "-cp" , "animals-demo-1.0-SNAPSHOT-jar-with-dependencies.jar", "-Dotel.exporter.otlp.endpoint=http://otel-collector:4317/", "-Dotel.service.name=animal-app", "io.opentelemetry.examples.animal.AnimalApplication"]
