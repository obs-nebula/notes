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


## [opentelemetry-js/packages/](https://github.com/open-telemetry/opentelemetry-js/tree/main/packages)

### opentelemetry-context-async-hooks

This package provides two [`ContextManager`](https://open-telemetry.github.io/opentelemetry-js/interfaces/_opentelemetry_api.ContextManager.html) implementations built on APIs from Node.js's [`async_hooks`][async-hooks-doc] module. If you're looking for a `ContextManager` to use in browser environments, consider [opentelemetry-context-zone](https://github.com/open-telemetry/opentelemetry-js/tree/main/packages/opentelemetry-context-zone) or [opentelemetry-context-zone-peer-dep](https://github.com/open-telemetry/opentelemetry-js/tree/main/packages/opentelemetry-context-zone-peer-dep).

### opentelemetry-context-zone-peer-dep

This module provides *Zone Context Manager with a peer dependency for [zone-js]* for Web applications.
If you use Angular you already have the [zone-js] and you should use this package.
If you don't have your own [zone-js] please use [@opentelemetry/context-zone]

### opentelemetry-context-zone

This module provides *Zone Context Manager with bundled [zone-js]* for Web applications.
If you have your own [zone-js] please use [@opentelemetry/context-zone-peer-dep]
If you use Angular it means you already have the [zone-js] and you should use [@opentelemetry/context-zone-peer-dep]

### opentelemetry-core

This package provides default implementations of the OpenTelemetry API for trace and metrics. It's intended for use both on the server and in the browser.

### opentelemetry-exporter-jaeger
(Deprecated) OpenTelemetry Jaeger Trace Exporter for Node.js

**NOTE: Support for `@opentelemetry/exporter-jaeger` will end March 2024, please use any of the following packages instead:**

- `@opentelemetry/exporter-trace-otlp-proto`
- `@opentelemetry/exporter-trace-otlp-grpc`
- `@opentelemetry/exporter-trace-otlp-http`

### opentelemetry-exporter-zipkin

OpenTelemetry Zipkin Trace Exporter allows the user to send collected traces to Zipkin.

### opentelemetry-propagator-b3

The OpenTelemetry b3 propagator package provides multiple propagator
implementations for systems using the b3 context format. See the
[b3 specification][b3-spec] for complete details.

### opentelemetry-propagator-jaeger

OpenTelemetry Jaeger propagator provides HTTP header propagation for systems that are using Jaeger HTTP header format.

### opentelemetry-resources

The OpenTelemetry Resource is an immutable representation of the entity producing telemetry. For example, a process producing telemetry that is running in a container on Kubernetes has a Pod name, it is in a namespace and possibly is part of a Deployment which also has a name. All three of these attributes can be included in the `Resource`.

### opentelemetry-sdk-trace-base

The `tracing` module contains the foundation for all tracing SDKs of [opentelemetry-js](https://github.com/open-telemetry/opentelemetry-js).

Used standalone, this module provides methods for manual instrumentation of code, offering full control over span creation for client-side JavaScript (browser) and Node.js.

It does **not** provide automated instrumentation of known libraries, context propagation for asynchronous invocations or distributed-context out-of-the-box.

### opentelemetry-sdk-trace-node

This module provides *automated instrumentation and tracing* for Node.js applications.

For manual instrumentation see the
[@opentelemetry/sdk-trace-base](https://github.com/open-telemetry/opentelemetry-js/tree/main/packages/opentelemetry-sdk-trace-base) package.

### opentelemetry-sdk-trace-web

This module provides *automated instrumentation and tracing* for Web applications.

For manual instrumentation see the
[@opentelemetry/sdk-trace-base](https://github.com/open-telemetry/opentelemetry-js/tree/main/packages/opentelemetry-sdk-trace-base) package.

### opentelemetry-semantic-conventions

Semantic Convention constants for use with the OpenTelemetry SDK/APIs. [This document][trace-semantic_conventions] defines standard attributes for traces.

### opentelemetry-shim-opentracing

OpenTracing shim allows existing OpenTracing instrumentation to report to OpenTelemetry

### sdk-metrics

This module contains the Metrics SDK of [opentelemetry-js](https://github.com/open-telemetry/opentelemetry-js).

Used standalone, this module provides methods for manual instrumentation of code, offering full control over recording metrics for client-side JavaScript (browser) and Node.js.

It does **not** provide automated instrumentation of known libraries or host environment metrics out-of-the-box.

### template

> TODO: description

## [opentelemetry-js-contrib/packages/](https://github.com/open-telemetry/opentelemetry-js-contrib/tree/main/packages)

### opentelemetry-host-metrics

This module provides automatic collection of Host Metrics which includes metrics for:

* CPU
* Memory
* Network

### opentelemetry-id-generator-aws-xray

The OpenTelemetry IdGenerator for AWS X-Ray generates trace IDs with its first four bytes set to the start time of the
trace followed by a unique identifier consisting of 12 bytes of randomly generated numbers. OpenTelemetry offers an
extension point which allows the usage of this custom IdGenerator as opposed to the out-of-the-box random IdGenerator,
enabling compatibility with AWS X-Ray.

### opentelemetry-propagation-utils

A collection of propagation utils for opentelemetry.

### opentelemetry-redis-common

This is an internal utils package used for the different redis instrumentations:

1. ioredis
2. redis
3. redis-4

### opentelemetry-test-utils

This is a internal utils package used across the contrib packages.
No guarantees are given to uses outside of [open-telemetry/opentelemetry-js-contrib](https://github.com/open-telemetry/opentelemetry-js-contrib/) repository.

