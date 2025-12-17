[//]: # (Source: https://www.jetbrains.com/help/idea/open-telemetry-tracing-and-metrics.html)
[//]: # (Downloaded: 2025-12-17 19:33:28)

## Spans

A Span represents a single operation with a trace. Spans can be sent to the endpoint and visualized in the Jaeger UI. Jaeger can be started in Docker. You can follow the link with the description on how to [set up Jaeger UI](https://www.jaegertracing.io/docs/1.18/opentelemetry/).

### Set up Span

  1. Start a Docker container with Jaeger. 

Use the following [binaries](https://www.jaegertracing.io/download/) to download Jaeger.

To start the Jaeger container, run the following code in the terminal:

docker run -d --name jaeger \ -e COLLECTOR_ZIPKIN_HTTP_PORT=9411 \ -e COLLECTOR_OTLP_ENABLED=true \ -p 6831:6831/udp \ -p 6832:6832/udp \ -p 5778:5778 \ -p 16686:16686 \ -p 4317:4317 \ -p 4318:4318 \ -p 14250:14250 \ -p 14268:14268 \ -p 14269:14269 \ -p 9411:9411 \ jaegertracing/all-in-one:1.38 

  2. Go to localhost:16686 to see the spans in Jaeger UI. 

The trace endpoint can be defined with property:

idea.diagnostic.opentelemetry.otlp

In case the flag is true, its value is set to default: http://127.0.0.1:4318/



