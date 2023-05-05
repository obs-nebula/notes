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


## [opentelemetry-js-contrib/detectors/](https://github.com/open-telemetry/opentelemetry-js-contrib/tree/main/detectors/node)

### opentelemetry-resource-detector-alibaba-cloud

Resource detector for Alibaba Cloud.

### opentelemetry-resource-detector-aws

Resource detector for Amazon Web Services.

### opentelemetry-resource-detector-container

Resource detector for container id.

### opentelemetry-resource-detector-gcp

Resource detector for Google Cloud Platform.

### opentelemetry-resource-detector-github

Resource detector for GitHub Actions.

Detects `GITHUB_*` environment variables [specified here](https://docs.github.com/en/free-pro-team@latest/actions/reference/environment-variables) and adds as attributes on a resource.

This is useful for collecting telemetry in GitHub Actions-powered CI/CD workflows.

### opentelemetry-resource-detector-instana

This resource detector will detect the Instana agent to register the Opentelemetry as a Node.js process. The created resource will be automatically merged with the existing resources and contains the real PID, which is returned from the Instana agent. This mechanism is needed to connect the Node.js Otel process with the incoming Opentelemetry spans.

## [opentelemetry-js-contrib/metapackages/](https://github.com/open-telemetry/opentelemetry-js-contrib/tree/main/metapackages)

### auto-instrumentations-node

This module provides a way to auto instrument any Node application to capture telemetry from a number of popular libraries and frameworks.
You can export the telemetry data in a variety of formats. Exporters, samplers, and more can be configured via [environment variables][env-var-url].
The net result is the ability to gather telemetry data from a Node application without any code changes.

This module also provides a simple way to manually initialize multiple Node instrumentations for use with the OpenTelemetry SDK.

### auto-instrumentations-web

Same as above, but for web.


## [opentelemetry-js-contrib/propagators/](https://github.com/open-telemetry/opentelemetry-js-contrib/tree/main/propagators)

### opentelemetry-propagator-aws-xray

The OpenTelemetry Propagator for AWS X-Ray provides HTTP header propagation for systems that are using AWS `X-Amzn-Trace-Id` format.
This propagator translates the OpenTelemetry SpanContext into the equivalent AWS header format, for use with the OpenTelemetry JS SDK.
`TraceState` is currently not propagated.


### opentelemetry-propagator-grpc-census-binary

OpenTelemetry gRPC Census propagator provides gRPC header propagation for systems that use the OpenCensus 'grpc-trace-bin' binary header format. This allows for context propagation when either:

* incoming gRPC calls come from services already instrumented using OpenCensus
* outgoing gRPC calls go to services already instrumented using OpenCensus

This propagator works in conjunction with the OpenTelemetry [gRPC plugin](https://github.com/open-telemetry/opentelemetry-js/tree/main/packages/exporter-trace-otlp-grpc).


### opentelemetry-propagator-instana

The OpenTelemetry Propagator for Instana provides HTTP header propagation for systems that are using IBM Observability by Instana.
This propagator translates the Instana trace correlation headers (`X-INSTANA-T/X-INSTANA-S/X-INSTANA-L`) into the OpenTelemetry `SpanContext`, and vice versa.
It does not handle `TraceState`.

### opentelemetry-propagator-ot-trace

???


## [opentelemetry-js-contrib/plugins/node](https://github.com/open-telemetry/opentelemetry-js-contrib/tree/main/plugins/node)

### instrumentation-amqplib

This module provides automatic instrumentation for the [`amqplib`](https://www.npmjs.com/package/amqplib) (RabbitMQ) module, which may be loaded using the [`@opentelemetry/sdk-trace-node`](https://github.com/open-telemetry/opentelemetry-js/tree/main/packages/opentelemetry-sdk-trace-node) package and is included in the [`@opentelemetry/auto-instrumentations-node`](https://www.npmjs.com/package/@opentelemetry/auto-instrumentations-node) bundle.

### instrumentation-dataloader

This module provides automatic instrumentation for the injection of trace context to [`dataloader`](https://www.npmjs.com/package/dataloader), which may be loaded using the [`@opentelemetry/sdk-trace-node`](https://github.com/open-telemetry/opentelemetry-js/tree/main/packages/opentelemetry-sdk-trace-node) package and is included in the [`@opentelemetry/auto-instrumentations-node`](https://www.npmjs.com/package/@opentelemetry/auto-instrumentations-node) bundle.


### instrumentation-fs

This module provides automatic instrumentation for the [`fs`](http://nodejs.org/dist/latest/docs/api/fs.html) module, which may be loaded using the [`@opentelemetry/sdk-trace-node`](https://github.com/open-telemetry/opentelemetry-js/tree/main/packages/opentelemetry-sdk-trace-node) package and is included in the [`@opentelemetry/auto-instrumentations-node`](https://www.npmjs.com/package/@opentelemetry/auto-instrumentations-node) bundle.

### instrumentation-lru-memoizer

This module provides automatic instrumentation for the [`lru-memorizer`](https://github.com/jfromaniello/lru-memoizer) module, which may be loaded using the [`@opentelemetry/sdk-trace-node`](https://github.com/open-telemetry/opentelemetry-js/tree/main/packages/opentelemetry-sdk-trace-node) package and is included in the [`@opentelemetry/auto-instrumentations-node`](https://www.npmjs.com/package/@opentelemetry/auto-instrumentations-node) bundle.

### instrumentation-mongoose

This module provides automatic instrumentation for the [`mongoose`](https://github.com/Automattic/mongoose) module, which may be loaded using the [`@opentelemetry/sdk-trace-node`](https://github.com/open-telemetry/opentelemetry-js/tree/main/packages/opentelemetry-sdk-trace-node) package and is included in the [`@opentelemetry/auto-instrumentations-node`](https://www.npmjs.com/package/@opentelemetry/auto-instrumentations-node) bundle.

### instrumentation-socket.io

This module provides automatic instrumentation for the [`socket.io`](https://github.com/socketio/socket.io) module, which may be loaded using the [`@opentelemetry/sdk-trace-node`](https://github.com/open-telemetry/opentelemetry-js/tree/main/packages/opentelemetry-sdk-trace-node) package and is included in the [`@opentelemetry/auto-instrumentations-node`](https://www.npmjs.com/package/@opentelemetry/auto-instrumentations-node) bundle.

### instrumentation-tedious

This module provides automatic instrumentation for the [`tedious`](https://github.com/tediousjs/tedious) module, which may be loaded using the [`@opentelemetry/sdk-trace-node`](https://github.com/open-telemetry/opentelemetry-js/tree/main/packages/opentelemetry-sdk-trace-node) package and is included in the [`@opentelemetry/auto-instrumentations-node`](https://www.npmjs.com/package/@opentelemetry/auto-instrumentations-node) bundle.

### opentelemetry-instrumentation-aws-lambda

This module provides automatic instrumentation for the [`AWS Lambda`](https://docs.aws.amazon.com/lambda/latest/dg/nodejs-handler.html) module, which may be loaded using the [`@opentelemetry/sdk-trace-node`](https://github.com/open-telemetry/opentelemetry-js/tree/main/packages/opentelemetry-sdk-trace-node) package and is included in the [`@opentelemetry/auto-instrumentations-node`](https://www.npmjs.com/package/@opentelemetry/auto-instrumentations-node) bundle.

### opentelemetry-instrumentation-aws-sdk

This module provides automatic instrumentation for the [`aws-sdk` v2](https://docs.aws.amazon.com/AWSJavaScriptSDK/latest/) and [`@aws-sdk` v3](https://github.com/aws/aws-sdk-js-v3) modules, which may be loaded using the [`@opentelemetry/sdk-trace-node`](https://github.com/open-telemetry/opentelemetry-js/tree/main/packages/opentelemetry-sdk-trace-node) package and is included in the [`@opentelemetry/auto-instrumentations-node`](https://www.npmjs.com/package/@opentelemetry/auto-instrumentations-node) bundle.

### opentelemetry-instrumentation-bunyan

This module provides automatic instrumentation for the injection of trace context to [`bunyan`](https://www.npmjs.com/package/bunyan), which may be loaded using the [`@opentelemetry/sdk-trace-node`](https://github.com/open-telemetry/opentelemetry-js/tree/main/packages/opentelemetry-sdk-trace-node) package and is included in the [`@opentelemetry/auto-instrumentations-node`](https://www.npmjs.com/package/@opentelemetry/auto-instrumentations-node) bundle.


### opentelemetry-instrumentation-cassandra

This module provides automatic instrumentation for the injection of trace context to [`cassandra-driver`](https://www.npmjs.com/package/cassandra-driver), which may be loaded using the [`@opentelemetry/sdk-trace-node`](https://github.com/open-telemetry/opentelemetry-js/tree/main/packages/opentelemetry-sdk-trace-node) package and is included in the [`@opentelemetry/auto-instrumentations-node`](https://www.npmjs.com/package/@opentelemetry/auto-instrumentations-node) bundle.


### opentelemetry-instrumentation-connect

This module provides automatic instrumentation for the [`connect`](https://github.com/senchalabs/connect) module, which may be loaded using the [`@opentelemetry/sdk-trace-node`](https://github.com/open-telemetry/opentelemetry-js/tree/main/packages/opentelemetry-sdk-trace-node) package and is included in the [`@opentelemetry/auto-instrumentations-node`](https://www.npmjs.com/package/@opentelemetry/auto-instrumentations-node) bundle.

### opentelemetry-instrumentation-dns

This module provides automatic instrumentation for the [`dns`](http://nodejs.org/dist/latest/docs/api/dns.html) module, which may be loaded using the [`@opentelemetry/sdk-trace-node`](https://github.com/open-telemetry/opentelemetry-js/tree/main/packages/opentelemetry-sdk-trace-node) package and is included in the [`@opentelemetry/auto-instrumentations-node`](https://www.npmjs.com/package/@opentelemetry/auto-instrumentations-node) bundle.

### opentelemetry-instrumentation-express

This module provides automatic instrumentation for the [`express`](https://github.com/expressjs/express) module, which may be loaded using the [`@opentelemetry/sdk-trace-node`](https://github.com/open-telemetry/opentelemetry-js/tree/main/packages/opentelemetry-sdk-trace-node) package and is included in the [`@opentelemetry/auto-instrumentations-node`](https://www.npmjs.com/package/@opentelemetry/auto-instrumentations-node) bundle.

This instrumentation relies on HTTP calls to also be instrumented. Make sure you install and enable both, otherwise you will not see any spans being exported from the instrumentation.

### opentelemetry-instrumentation-fastify

This module provides automatic instrumentation for the [`fastify`](https://www.fastify.io/) module, which may be loaded using the [`@opentelemetry/sdk-trace-node`](https://github.com/open-telemetry/opentelemetry-js/tree/main/packages/opentelemetry-sdk-trace-node) package and is included in the [`@opentelemetry/auto-instrumentations-node`](https://www.npmjs.com/package/@opentelemetry/auto-instrumentations-node) bundle.

This instrumentation relies on HTTP calls to also be instrumented. Make sure you install and enable both, otherwise you will have spans that are not connected with each other.

### opentelemetry-instrumentation-generic-pool

This module provides automatic instrumentation for the [`generic-pool`](https://github.com/coopernurse/node-pool) module, creating a span for every acquire call, which may be loaded using the [`@opentelemetry/sdk-trace-node`](https://github.com/open-telemetry/opentelemetry-js/tree/main/packages/opentelemetry-sdk-trace-node) package and is included in the [`@opentelemetry/auto-instrumentations-node`](https://www.npmjs.com/package/@opentelemetry/auto-instrumentations-node) bundle.


### opentelemetry-instrumentation-graphql

This module provides automatic instrumentation and tracing for GraphQL in Node.js applications, which may be loaded using the [`@opentelemetry/sdk-trace-node`](https://github.com/open-telemetry/opentelemetry-js/tree/main/packages/opentelemetry-sdk-trace-node) package and is included in the [`@opentelemetry/auto-instrumentations-node`](https://www.npmjs.com/package/@opentelemetry/auto-instrumentations-node) bundle.

*Note*: graphql plugin instruments graphql directly. it should work with any package that wraps the graphql package (e.g apollo).

### opentelemetry-instrumentation-hapi

This module provides automatic instrumentation for the [Hapi Framework](https://hapi.dev)(`@hapi/hapi`)package, which may be loaded using the [`@opentelemetry/sdk-trace-node`](https://github.com/open-telemetry/opentelemetry-js/tree/main/packages/opentelemetry-sdk-trace-node) package and is included in the [`@opentelemetry/auto-instrumentations-node`](https://www.npmjs.com/package/@opentelemetry/auto-instrumentations-node) bundle.

### opentelemetry-instrumentation-ioredis

This module provides automatic instrumentation for the [`ioredis`](https://github.com/luin/ioredis) module, which may be loaded using the [`@opentelemetry/sdk-trace-node`](https://github.com/open-telemetry/opentelemetry-js/tree/main/packages/opentelemetry-sdk-trace-node) package and is included in the [`@opentelemetry/auto-instrumentations-node`](https://www.npmjs.com/package/@opentelemetry/auto-instrumentations-node) bundle.

### opentelemetry-instrumentation-knex

This module provides automatic instrumentation for the [`knex`](https://github.com/knex/knex) module, which may be loaded using the [`@opentelemetry/sdk-trace-node`](https://github.com/open-telemetry/opentelemetry-js/tree/main/packages/opentelemetry-sdk-trace-node) package and is included in the [`@opentelemetry/auto-instrumentations-node`](https://www.npmjs.com/package/@opentelemetry/auto-instrumentations-node) bundle. This module allows the user to automatically collect trace data and export them to their backend of choice.

### opentelemetry-instrumentation-koa

This module provides automatic instrumentation for the [Koa](https://github.com/koajs/koa) module, which may be loaded using the [`@opentelemetry/sdk-trace-node`](https://github.com/open-telemetry/opentelemetry-js/tree/main/packages/opentelemetry-sdk-trace-node) package and is included in the [`@opentelemetry/auto-instrumentations-node`](https://www.npmjs.com/package/@opentelemetry/auto-instrumentations-node) bundle.

### opentelemetry-instrumentation-memcached

This module provides automatic instrumentation for the [`memcached@>=2.2.0`][repo-url] module, which may be loaded using the [`@opentelemetry/sdk-trace-node`](https://github.com/open-telemetry/opentelemetry-js/tree/main/packages/opentelemetry-sdk-trace-node) package and is included in the [`@opentelemetry/auto-instrumentations-node`](https://www.npmjs.com/package/@opentelemetry/auto-instrumentations-node) bundle.


### opentelemetry-instrumentation-mongodb

This module provides automatic instrumentation for the [`mongodb`](https://github.com/mongodb/node-mongodb-native) module, which may be loaded using the [`@opentelemetry/sdk-trace-node`](https://github.com/open-telemetry/opentelemetry-js/tree/main/packages/opentelemetry-sdk-trace-node) package and is included in the [`@opentelemetry/auto-instrumentations-node`](https://www.npmjs.com/package/@opentelemetry/auto-instrumentations-node) bundle.

### opentelemetry-instrumentation-mysql

This module provides automatic instrumentation for the [`mysql`](https://www.npmjs.com/package/mysql) module, which may be loaded using the [`@opentelemetry/sdk-trace-node`](https://github.com/open-telemetry/opentelemetry-js/tree/main/packages/opentelemetry-sdk-trace-node) package and is included in the [`@opentelemetry/auto-instrumentations-node`](https://www.npmjs.com/package/@opentelemetry/auto-instrumentations-node) bundle.

### opentelemetry-instrumentation-mysql2

This module provides automatic instrumentation for the [`mysql2`](https://github.com/sidorares/node-mysql2) module, which may be loaded using the [`@opentelemetry/sdk-trace-node`](https://github.com/open-telemetry/opentelemetry-js/tree/main/packages/opentelemetry-sdk-trace-node) package and is included in the [`@opentelemetry/auto-instrumentations-node`](https://www.npmjs.com/package/@opentelemetry/auto-instrumentations-node) bundle.


### opentelemetry-instrumentation-nestjs-core

This module provides automatic instrumentation for the [Nest framework][pkg-web-url] module, which may be loaded using the [`@opentelemetry/sdk-trace-node`](https://github.com/open-telemetry/opentelemetry-js/tree/main/packages/opentelemetry-sdk-trace-node) package and is included in the [`@opentelemetry/auto-instrumentations-node`](https://www.npmjs.com/package/@opentelemetry/auto-instrumentations-node) bundle.


### opentelemetry-instrumentation-net

This module provides automatic instrumentation for the [`net`](http://nodejs.org/dist/latest/docs/api/net.html) module, which may be loaded using the [`@opentelemetry/sdk-trace-node`](https://github.com/open-telemetry/opentelemetry-js/tree/main/packages/opentelemetry-sdk-trace-node) package and is included in the [`@opentelemetry/auto-instrumentations-node`](https://www.npmjs.com/package/@opentelemetry/auto-instrumentations-node) bundle.

Supports both TCP and IPC connections.

### opentelemetry-instrumentation-pg

This module provides automatic instrumentation for the [`pg`](https://github.com/brianc/node-postgres)module, which may be loaded using the [`@opentelemetry/sdk-trace-node`](https://github.com/open-telemetry/opentelemetry-js/tree/main/packages/opentelemetry-sdk-trace-node) package and is included in the [`@opentelemetry/auto-instrumentations-node`](https://www.npmjs.com/package/@opentelemetry/auto-instrumentations-node) bundle.

### opentelemetry-instrumentation-pino

This module provides automatic instrumentation for injection of trace context for the [`pino`](https://www.npmjs.com/package/pino) module, which may be loaded using the [`@opentelemetry/sdk-trace-node`](https://github.com/open-telemetry/opentelemetry-js/tree/main/packages/opentelemetry-sdk-trace-node) package and is included in the [`@opentelemetry/auto-instrumentations-node`](https://www.npmjs.com/package/@opentelemetry/auto-instrumentations-node) bundle.


### opentelemetry-instrumentation-redis-4

This module provides automatic instrumentation for the [`redis@^4.0.0`](https://github.com/NodeRedis/node_redis) module, which may be loaded using the [`@opentelemetry/sdk-trace-node`](https://github.com/open-telemetry/opentelemetry-js/tree/main/packages/opentelemetry-sdk-trace-node) package and is included in the [`@opentelemetry/auto-instrumentations-node`](https://www.npmjs.com/package/@opentelemetry/auto-instrumentations-node) bundle.

### opentelemetry-instrumentation-redis

This module provides automatic instrumentation for the [`redis@^2.6.0`](https://github.com/NodeRedis/node_redis) module, which may be loaded using the [`@opentelemetry/sdk-trace-node`](https://github.com/open-telemetry/opentelemetry-js/tree/main/packages/opentelemetry-sdk-trace-node) package and is included in the [`@opentelemetry/auto-instrumentations-node`](https://www.npmjs.com/package/@opentelemetry/auto-instrumentations-node) bundle.


### opentelemetry-instrumentation-restify

This module provides automatic instrumentation for the [`restify`](https://github.com/restify/node-restify) module, which may be loaded using the [`@opentelemetry/sdk-trace-node`](https://github.com/open-telemetry/opentelemetry-js/tree/main/packages/opentelemetry-sdk-trace-node) package and is included in the [`@opentelemetry/auto-instrumentations-node`](https://www.npmjs.com/package/@opentelemetry/auto-instrumentations-node) bundle. It allows the user to automatically collect trace data and export them to their backend of choice.

### opentelemetry-instrumentation-router

This module provides automatic instrumentation for the [`router`](https://github.com/pillarjs/router) module, which may be loaded using the [`@opentelemetry/sdk-trace-node`](https://github.com/open-telemetry/opentelemetry-js/tree/main/packages/opentelemetry-sdk-trace-node) package and is included in the [`@opentelemetry/auto-instrumentations-node`](https://www.npmjs.com/package/@opentelemetry/auto-instrumentations-node) bundle. It allows the user to automatically collect trace data and export them to their backend of choice.

### opentelemetry-instrumentation-winston

This module provides automatic instrumentation for injection of trace context for the [`winston`](https://www.npmjs.com/package/winston) module, which may be loaded using the [`@opentelemetry/sdk-trace-node`](https://github.com/open-telemetry/opentelemetry-js/tree/main/packages/opentelemetry-sdk-trace-node) package and is included in the [`@opentelemetry/auto-instrumentations-node`](https://www.npmjs.com/package/@opentelemetry/auto-instrumentations-node) bundle.


## [opentelemetry-js-contrib/plugins/web](https://github.com/open-telemetry/opentelemetry-js-contrib/tree/main/plugins/web)

### opentelemetry-instrumentation-document-load

This module provides automatic instrumentation for *document load* for Web applications, which may be loaded using the [`@opentelemetry/sdk-trace-web`](https://www.npmjs.com/package/@opentelemetry/sdk-trace-web) package.

### opentelemetry-instrumentation-long-task

This module provides automatic instrumentation for [Long Task API][mdn-long-task] which may be loaded using the [`@opentelemetry/sdk-trace-web`](https://www.npmjs.com/package/@opentelemetry/sdk-trace-web) package. It creates spans from tasks that take more than 50 milliseconds, all of the data reported via [`PerformanceLongTaskTiming`][mdn-performance-long-task-timing] is included as span attributes.

### opentelemetry-instrumentation-user-interaction

This module provides automatic instrumentation for *user interactions* for Web applications, which may be loaded using the [`@opentelemetry/sdk-trace-web`](https://www.npmjs.com/package/@opentelemetry/sdk-trace-web) package.

This module can work either with [zone-js] or without it, with [zone-js] and ZoneContextManager it will fully support the async operations. Without [zone-js] it will still work but with limited support.
If you use Angular or [@opentelemetry/context-zone] you will have [zone-js] included.

### opentelemetry-plugin-react-load

This module provides automatic instrumentation for *React lifecycles* for Web applications, which may be loaded using the [`@opentelemetry/sdk-trace-web`](https://www.npmjs.com/package/@opentelemetry/sdk-trace-web) package.


##### total

```
➜  notes git:(main) ✗ grep -c "^###" packages.md
94
```