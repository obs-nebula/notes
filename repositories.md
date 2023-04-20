# Repositories

* [Supernova](https://github.com/obs-nebula/supernova) - This is our central repository.
  * We create new things here first, and then if make sense to create a new repository we can close the issue and continue on the created repository.
  * It's also a good place to create issues that affect multiple repositories.
* [check-traces](https://github.com/obs-nebula/check-traces) - The purpose of this repository is to ensure that a basic Express app's traces are correctly generated and successfully exported to the final destination which is Jaeger. So we can make safer modifications and experiments according to the evolution of the APIs of the OTEL-JS modules. Since we are using `@opentelemetry/exporter-trace-otlp-http` instead of `@opentelemetry/exporter-jaeger` we can guarantee that the results of CI running on the main branch will be the same for any dependency updates for the other branches.
  * Branches:
    * [meta-package](https://github.com/obs-nebula/check-traces/tree/meta-package) - Same as the main branch but using the OTEL-JS meta-package instead `@opentelemetry/auto-instrumentations-node`.
    * [sdk-node](https://github.com/obs-nebula/check-traces/tree/sdk-node) - Same as the main branch but using the `@opentelemetry/sdk-node` to enable and disable telemetry via environment variable. This works both locally and inside OpenShift.
    * [otelcol-auto-instrumentation](https://github.com/obs-nebula/check-traces/tree/otelcol-auto-instrumentation) - This branch is using auto-instrumentation injection with OTELCOL Operator. This was used to make [this comparison](https://github.com/obs-nebula/check-traces/issues/9#issuecomment-1489380770) 
* [check-traces-manual](https://github.com/obs-nebula/check-traces-manual) - Same as `check-traces`, but using manual instrumentation.
* [desktop-electron](https://github.com/obs-nebula/desktop-electron) - A really basic Desktop Electron app that is part of the `function-five` demo to call the first and the last function outside the cloud.
* [frontend-react](https://github.com/obs-nebula/frontend-react) - Repository containing a basic back-end and a front-end, used to apply OpenTelemetry-JS (Web) for trace instrumentation. This repository is referenced in the following [blog post](https://developers.redhat.com/articles/2023/03/22/how-enable-opentelemetry-traces-react-applications#further_reading)
  * Branches:
    * [batch](https://github.com/obs-nebula/frontend-react/tree/batch) - Same as the main branch but using `BatchSpanProcessor` instead of `SimpleSpanProcessor`.
    * [deploy](https://github.com/obs-nebula/frontend-react/tree/deploy) - Same as the main branch but intended to be deployed to OpenShift - Blocked by external access restrictions (the browser).
* [function-five](https://github.com/obs-nebula/function-five) - Knative-functions demo (WIP)
  * Branches:
    * [otel](https://github.com/obs-nebula/function-five/tree/otel) - Basic experiments with manual instrumentation 
* [hyperfoil-test](https://github.com/obs-nebula/hyperfoil-test) - Repository containing a demo that uses https://hyperfoil.io/ to compare the performance of some OpenTelemetry-JS plugins when applied to microservices.
  * Branches:
    * [console_exporter](https://github.com/obs-nebula/hyperfoil-test/tree/console_exporter) - Using OTEL-JS traces instrumentation and exporting the results to console.
    * [otelcol_exporter](https://github.com/obs-nebula/hyperfoil-test/tree/otelcol_exporter) - Using OTEL-JS traces instrumentation and exporting the results to OTELCOL.
* [osview](https://github.com/obs-nebula/osview) - A basic CLI used as an experiment to apply the OpenTelemetry signals, currently instrumented with metrics and traces.
* [perf-quest](https://github.com/obs-nebula/perf-quest) - This repository is an experimental meta-work related to [hyperfoil-test](https://github.com/obs-nebula/hyperfoil-test)
* [gamma-ray](https://github.com/obs-nebula/gamma-ray) - Nothing done, reserved for future experiments.
* [notes](https://github.com/obs-nebula/notes) - General notes and documentation.
