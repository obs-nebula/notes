# Packages

## [opentelemetry-js/experimental/packages/](https://github.com/open-telemetry/opentelemetry-js/tree/main/experimental/packages)

### api-events

This package provides everything needed to interact with the unstable OpenTelemetry Events API, including all TypeScript interfaces, enums, and no-op implementations. It is intended for use both on the server and in the browser.

### api-logs

This package provides everything needed to interact with the unstable OpenTelemetry Logs API, including all TypeScript interfaces, enums, and no-op implementations. It is intended for use both on the server and in the browser.

The logs API is considered alpha software and there is no guarantee of stability or long-term support. When the API is stabilized, it will be made available and supported long-term in the `@opentelemetry/api` package and this package will be deprecated.

### exporter-trace-otlp-grpc

This module provides exporter for node to be used with OTLP (`grpc`) compatible receivers.
Compatible with [opentelemetry-collector][opentelemetry-collector-url] versions `>=0.16 <=0.50`.

### exporter-trace-otlp-http

This module provides exporter for web and node to be used with OTLP (`http/json`) compatible receivers.
Compatible with [opentelemetry-collector][opentelemetry-collector-url] versions `>=0.48 <=0.50`.

### exporter-trace-otlp-proto

This module provides exporter for node to be used with OTLP (`http/protobuf`) compatible receivers.
Compatible with [opentelemetry-collector][opentelemetry-collector-url] versions `>=0.32 <=0.50`.

### opentelemetry-browser-detector

This module provides detector for browser environments

### opentelemetry-exporter-metrics-otlp-grpc

This module provides exporter for node to be used with OTLP (`grpc`) compatible receivers.
Compatible with [opentelemetry-collector][opentelemetry-collector-url] versions `>=0.16 <=0.53`.

### opentelemetry-exporter-metrics-otlp-http

This module provides exporter for web and node to be used with OTLP (`http/json`) compatible receivers.
Compatible with [opentelemetry-collector][opentelemetry-collector-url] versions `>=0.52 <=0.53`.

### opentelemetry-exporter-metrics-otlp-proto

This module provides exporter for node to be used with OTLP (`http/protobuf`) compatible receivers.
Compatible with [opentelemetry-collector][opentelemetry-collector-url] versions `>=0.32 <=0.53`.

### opentelemetry-exporter-prometheus

The OpenTelemetry Prometheus Metrics Exporter allows the user to send collected [OpenTelemetry Metrics](https://github.com/open-telemetry/opentelemetry-js/tree/main/packages/sdk-metrics) to Prometheus.

### opentelemetry-instrumentation-fetch

This module provides auto instrumentation for web using fetch.

### opentelemetry-instrumentation-grpc

This module provides automatic instrumentation for [`grpc`](https://grpc.github.io/grpc/node/) and [`@grpc/grpc-js`](https://grpc.io/blog/grpc-js-1.0/). Currently, version [`1.x`](https://www.npmjs.com/package/grpc?activeTab=versions) of `grpc` and version [`1.x`](https://www.npmjs.com/package/@grpc/grpc-js?activeTab=versions) of `@grpc/grpc-js` is supported.

For automatic instrumentation see the
[@opentelemetry/sdk-trace-node](https://github.com/open-telemetry/opentelemetry-js/tree/main/packages/opentelemetry-sdk-trace-node) package.

### opentelemetry-instrumentation-http

This module provides automatic instrumentation for [`http`](https://nodejs.org/api/http.html) and [`https`](https://nodejs.org/api/https.html).

For automatic instrumentation see the
[@opentelemetry/sdk-trace-node](https://github.com/open-telemetry/opentelemetry-js/tree/main/packages/opentelemetry-sdk-trace-node) package.

### opentelemetry-instrumentation-xml-http-request

This module provides auto instrumentation for web using XMLHttpRequest .

### opentelemetry-instrumentation

??

### opentelemetry-sdk-node

This package provides the full OpenTelemetry SDK for Node.js including tracing and metrics.

### otlp-exporter-base

**Note: This package is intended for internal use only.**

This module provides a base exporter for web and node to be used with [opentelemetry-collector][opentelemetry-collector-url].

### otlp-grpc-exporter-base

**Note: This package is intended for internal use only.**

This module provides a gRPC exporter base for Node.js (browsers not supported) to be used with [opentelemetry-collector][opentelemetry-collector-url].

### otlp-proto-exporter-base

**Note: This package is intended for internal use only.**

This module provides a OTLP-http/protobuf exporter base for Node.js (browsers not supported) to be used with [opentelemetry-collector][opentelemetry-collector-url].

### otlp-transformer

**Note: This package is intended for internal use only.**

This package provides everything needed to serialize [OpenTelemetry SDK][sdk] traces, metrics and logs into the [OpenTelemetry Protocol][otlp] format.

### exporter-logs-otlp-grpc

This module provides an exporter for OTLP gRPC logs using protocol version `v0.18`.

### opentelemetry-shim-opencensus

> **Note**
> This package is in active development and has not yet been released. You cannot install this
> package from NPM yet.

OpenCensus shim allows existing OpenCensus instrumentation to report to OpenTelemetry. This
allows you to incrementally migrate your existing OpenCensus instrumentation to OpenTelemetry.
More details are available in the [OpenCensus Compatibility Specification](https://github.com/open-telemetry/opentelemetry-specification/blob/main/specification/compatibility/opencensus.md).

### sdk-logs

OpenTelemetry logs module contains the foundation for all logs SDKs of [opentelemetry-js](https://github.com/open-telemetry/opentelemetry-js).

Used standalone, this module provides methods for manual instrumentation of code, offering full control over recording logs for client-side JavaScript (browser) and Node.js.

It does **not** provide automated instrumentation of known libraries or host environment logs out-of-the-box.

