> Notes based on Jaeger/documentation repository. This is basically a reduced version of https://github.com/jaegertracing/documentation.

* **Getting in touch**
  * [Slack channel](https://cloud-native.slack.com/archives/CGG7NFUJ3)
  * [Meetings](https://docs.google.com/document/d/1ZuBAwTJvQN7xkWVvEFXj5WU9_JmS5TPiNbxCJSvPqX0/)
* **Downloads**
  * [Executable binaries](https://github.com/jaegertracing/jaeger/releases/)
  * [Docker images](https://hub.docker.com/r/jaegertracing/)
* **Index**
  * Jaeger, inspired by `Dapper` and `OpenZipkin`, is a distributed tracing system released as open source by `Uber Technologies` and it is used for monitoring and troubleshooting microservices-based distributed systems.
* **Apis**
  * **Span reporting APIs**
    * Agent and Collector are the two components of the Jaeger backend that can receive spans.
      * **OpenTelemetry Protocol**
        * Jaeger can receive trace data from the OpenTelemetry SDKs in their native `OTLP`. It is no longer necessary to configure the OpenTelemetry SDKs with Jaeger exporters, nor deploy the OpenTelemetry Collectors between the OpenTelemetry SDKs and the Jaeger backend. The `OTLP` data is accepted in these formats: binary gRPC, Protobuf over HTTP, JSON over HTTP.
        * As `@opentelemetry/exporter-jaeger` was deprecated the following formats are out of our scope, please go to the official Jaeger docs for more details.
          * Thrift over UDP - `OBS-NEBULA-OUT-OF-SCOPE`
          * Thrift over HTTP - `OBS-NEBULA-OUT-OF-SCOPE`
          * JSON over HTTP - `OBS-NEBULA-OUT-OF-SCOPE`
          * Protobuf via gRPC - `OBS-NEBULA-OUT-OF-SCOPE`
          * Zipkin Formats - `OBS-NEBULA-OUT-OF-SCOPE`
  * **Trace retrieval APIs**
    * Traces saved in the storage can be retrieved by calling Jaeger Query Service as following:
      * gRPC/Protobuf - The recommended way for programmatically retrieving traces and other data is via `jaeger.api_v2.QueryService` gRPC endpoint defined in [query.proto](https://github.com/jaegertracing/jaeger-idl/blob/main/proto/api_v2/query.proto) IDL file.
      * HTTP JSON (internal) - Jaeger UI communicates with Jaeger Query Service via JSON API. For example, a trace can be retrieved via GET request to `https://jaeger-query:16686/api/traces/{trace-id-hex-string}`. This JSON API is intentionally undocumented and subject to change.
  * **Remote Storage API** - `OBS-NEBULA-OUT-OF-SCOPE`
  * 