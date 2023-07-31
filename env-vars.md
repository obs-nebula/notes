# Environment variables

Some environment variables are described here:
https://github.com/open-telemetry/opentelemetry-specification/blob/main/specification/configuration/sdk-environment-variables.md#general-sdk-configuration

* OTEL_EXPORTER_JAEGER_AGENT_HOST
  * Deprecated https://github.com/open-telemetry/opentelemetry-js/tree/main/packages/opentelemetry-exporter-jaeger#deprecated-opentelemetry-jaeger-trace-exporter-for-nodejs
* OTEL_EXPORTER_JAEGER_AGENT_PORT
  * Deprecated https://github.com/open-telemetry/opentelemetry-js/tree/main/packages/opentelemetry-exporter-jaeger#deprecated-opentelemetry-jaeger-trace-exporter-for-nodejs
* OTEL_EXPORTER_JAEGER_ENDPOINT
  * Deprecated https://github.com/open-telemetry/opentelemetry-js/tree/main/packages/opentelemetry-exporter-jaeger#deprecated-opentelemetry-jaeger-trace-exporter-for-nodejs
* OTEL_EXPORTER_JAEGER_PASSWORD
  * Deprecated https://github.com/open-telemetry/opentelemetry-js/tree/main/packages/opentelemetry-exporter-jaeger#deprecated-opentelemetry-jaeger-trace-exporter-for-nodejs
* OTEL_EXPORTER_JAEGER_USER
  * Deprecated https://github.com/open-telemetry/opentelemetry-js/tree/main/packages/opentelemetry-exporter-jaeger#deprecated-opentelemetry-jaeger-trace-exporter-for-nodejs
* OTEL_EXPORTER_OTLP_CERTIFICATE
  * todo
* OTEL_EXPORTER_OTLP_CLIENT_CERTIFICATE
  * todo
* OTEL_EXPORTER_OTLP_CLIENT_KEY
  * todo
* OTEL_EXPORTER_OTLP_COMPRESSION
  * todo
* OTEL_EXPORTER_OTLP_ENDPOINT
  * todo
* OTEL_EXPORTER_OTLP_HEADERS
  * todo
* OTEL_EXPORTER_OTLP_INSECURE
  * todo
* OTEL_EXPORTER_OTLP_LOGS_CERTIFICATE
  * todo
* OTEL_EXPORTER_OTLP_LOGS_CLIENT_CERTIFICATE
  * todo
* OTEL_EXPORTER_OTLP_LOGS_CLIENT_KEY
  * todo
* OTEL_EXPORTER_OTLP_LOGS_COMPRESSION
  * todo
* OTEL_EXPORTER_OTLP_LOGS_ENDPOINT
  * todo
* OTEL_EXPORTER_OTLP_LOGS_HEADERS
  * todo
* OTEL_EXPORTER_OTLP_LOGS_INSECURE
  * todo
* OTEL_EXPORTER_OTLP_LOGS_PROTOCOL
  * todo
* OTEL_EXPORTER_OTLP_LOGS_TIMEOUT
  * todo
* OTEL_EXPORTER_OTLP_METRICS_CERTIFICATE
  * todo
* OTEL_EXPORTER_OTLP_METRICS_CLIENT_CERTIFICATE
  * todo
* OTEL_EXPORTER_OTLP_METRICS_CLIENT_KEY
  * todo
* OTEL_EXPORTER_OTLP_METRICS_COMPRESSION
  * todo
* OTEL_EXPORTER_OTLP_METRICS_ENDPOINT
  * todo
* OTEL_EXPORTER_OTLP_METRICS_HEADERS
  * todo
* OTEL_EXPORTER_OTLP_METRICS_INSECURE
  * todo
* OTEL_EXPORTER_OTLP_METRICS_PROTOCOL
  * todo
* OTEL_EXPORTER_OTLP_METRICS_TEMPORALITY_PREFERENCE
  * todo
* OTEL_EXPORTER_OTLP_METRICS_TIMEOUT
  * todo
* OTEL_EXPORTER_OTLP_PROTOCOL
  * todo
* OTEL_EXPORTER_OTLP_TIMEOUT
  * todo
* OTEL_EXPORTER_OTLP_TRACES_CERTIFICATE
  * todo
* OTEL_EXPORTER_OTLP_TRACES_CLIENT_CERTIFICATE
  * todo
* OTEL_EXPORTER_OTLP_TRACES_CLIENT_KEY
  * todo
* OTEL_EXPORTER_OTLP_TRACES_COMPRESSION
  * todo
* OTEL_EXPORTER_OTLP_TRACES_ENDPOINT
  * todo
* OTEL_EXPORTER_OTLP_TRACES_HEADERS
  * todo
* OTEL_EXPORTER_OTLP_TRACES_INSECURE
  * todo
* OTEL_EXPORTER_OTLP_TRACES_PROTOCOL
  * todo
* OTEL_EXPORTER_OTLP_TRACES_TIMEOUT
  * todo
* OTEL_GRAPHQL_DATA_SYMBOL
  * todo
* OTEL_LAMBDA_DISABLE_AWS_CONTEXT_PROPAGATION
  * todo
* OTEL_NO_PATCH_MODULES
  * todo
* OTEL_NODE_RESOURCE_DETECTORS
  * todo
* OTEL_OPEN_SPANS
  * todo
* OTEL_PATCHED_SYMBOL
  * todo
* OTEL_SAMPLING_PROBABILITY
  * Sampling configuration via environment variable has changed. If you were using `OTEL_SAMPLING_PROBABILITY` then you should replace it with `OTEL_TRACES_SAMPLER=parentbased_traceidratio` and `OTEL_TRACES_SAMPLER_ARG=<number>` where `<number>` is a number in the [0..1] range, e.g. "0.25". Default is 1.0 if unset.
  * https://github.com/open-telemetry/opentelemetry-js#018x-to-0190
* OTEL_SPAN_ATTRIBUTE_PER_EVENT_COUNT_LIMIT
  * todo
* OTEL_SPAN_ATTRIBUTE_PER_LINK_COUNT_LIMIT
  * todo