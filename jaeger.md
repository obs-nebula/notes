> Notes based on Jaeger/documentation repository. This is basically a reduced version of https://github.com/jaegertracing/documentation/tree/main/content focused on obs-nebula scope only. 

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
          * Thrift over UDP - `OUT-OF-SCOPE`
          * Thrift over HTTP - `OUT-OF-SCOPE`
          * JSON over HTTP - `OUT-OF-SCOPE`
          * Protobuf via gRPC - `OUT-OF-SCOPE`
          * Zipkin Formats - `OUT-OF-SCOPE`
  * **Trace retrieval APIs**
    * Traces saved in the storage can be retrieved by calling Jaeger Query Service as following:
      * gRPC/Protobuf - The recommended way for programmatically retrieving traces and other data is via `jaeger.api_v2.QueryService` gRPC endpoint defined in [query.proto](https://github.com/jaegertracing/jaeger-idl/blob/main/proto/api_v2/query.proto) IDL file.
      * HTTP JSON (internal) - Jaeger UI communicates with Jaeger Query Service via JSON API. For example, a trace can be retrieved via GET request to `https://jaeger-query:16686/api/traces/{trace-id-hex-string}`. This JSON API is intentionally undocumented and subject to change.
  * **Remote Storage API** - `OUT-OF-SCOPE`
  * **Remote Sampling Configuration** - `OUT-OF-SCOPE`
* **Architecture**
  * **Terminology** - All the terminology section makes sense to read directly in the [docs](https://github.com/jaegertracing/documentation/blob/main/content/docs/next-release/architecture.md#terminology)
  * The other sections talks about deployment options but we are going to stick with all-in-one binary and in-memory storage, so adding `OUT-OF-SCOPE` for this.
* cli.md, deployment.md, external-guides.md, faq.md, features.md as `OUT-OF-SCOPE`
* **Frontend UI**
  * We can use some flags to hide some parts of the UI, useful for sharing and screenshots
    * Example: `http://localhost:16686/trace/{trace-id}?uiEmbed=v0&uiTimelineHideMinimap=1&uiTimelineHideSummary=1`
* **Getting started**
  * The table explaining the exposed ports [link](https://www.jaegertracing.io/docs/1.43/getting-started/#all-in-one)
* **Monitoring**
  * By default Jaeger microservices expose metrics in Prometheus format.
  * `--metrics-http-route` specifies the name of the HTTP endpoint used to scrape the metrics (`/metrics` by default).
    * We are using it for check-traces and check-traces-manual repositories [link](https://github.com/obs-nebula/check-traces/blob/main/scripts/check-traces.sh#L1) to grep with the name of the service to know if the trace was sent or not.
  * Jaeger has the ability to trace some of its own components. That is why we can see `jaeger-query` populated in the Services dropdown.
* **Operator**
  * For the operator section we are going to stick with OpenShift usage (basically at [example/branch](https://github.com/obs-nebula/check-traces/tree/add-otelcol) level).
  * Makes sense for us to know about the section [Understanding Custom Resource Definitions](https://github.com/jaegertracing/documentation/blob/main/content/docs/next-release/operator.md#understanding-custom-resource-definitions) 
* performance-tuning.md `OUT-OF-SCOPE`
* **Sampling**
  * "This section only applies to classic Jaeger SDKs, which are now deprecated." We recommend using the [OpenTelemetry SDKs](https://opentelemetry.io).
  * Remote sampling: https://github.com/open-telemetry/opentelemetry-js/issues/692
* security.md `OUT-OF-SCOPE`
* spm.md, tools.md `OUT-OF-SCOPE`
* **Troubleshooting**
  * We are using the metrics endpoint in our check-traces repository for CI `curl http://jaeger-collector:14269/metrics` and we "grep" for the service's name to check if the traces were created and sent.
* windows.md `OUT-OF-SCOPE`