FROM busybox
ADD https://github.com/aws-observability/aws-otel-java-instrumentation/releases/download/v1.16.0/aws-opentelemetry-agent.jar javaagent.jar
RUN chmod -R go+r /javaagent.jar
