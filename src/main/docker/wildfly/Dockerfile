FROM quay.io/wildfly/wildfly:26.1.1.Final-2
USER root
RUN mkdir /app
COPY first-responder-demo.war  /app
WORKDIR /app
RUN wildfly-26.1.1.Final/bin/standalone.sh
CMD ["java", "-cp" , "animals-demo-1.0-SNAPSHOT-jar-with-dependencies.jar", "-Dotel.exporter.otlp.endpoint=http://otel-collector:4317/", "-Dotel.service.name=animal-app", "io.opentelemetry.examples.animal.AnimalApplication"]
