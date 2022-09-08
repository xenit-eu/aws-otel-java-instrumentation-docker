#AWS OTEL Java instrumentation Docker image
This is a project that will build a docker image containing the latest [aws-otel-java-instrumentation jar](https://github.com/aws-observability/aws-otel-java-instrumentation).
In this way it can be used for example with projects like the auto-instrumentation setup of the [opentelemetry-operator](https://github.com/open-telemetry/opentelemetry-operator)
```yaml
apiVersion: opentelemetry.io/v1alpha1
kind: Instrumentation
metadata:
  name: otel-auto-instrumentation
  namespace: alfresco
spec:
  exporter:
    endpoint: http://my-collector-xray-collector:4317
  java:
    image: hub.xenit.eu/customer-oup/aws-otel-java-agent:1.0.1
```

The project will automatically push a new version of the image with the help of dependabot. The version of the image will always follow the version of the aws-otel-java-instrumentation jar