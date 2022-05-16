# Overview

This example shows how to use [@opentelemetry/sdk-trace-web](https://github.com/open-telemetry/opentelemetry-js/tree/main/packages/opentelemetry-sdk-trace-web) with different plugins and setup to instrument your JavaScript code running with Deno.

## Installation

```sh
# from this directory
npm install
```

## Run the Application

```sh
# from this directory
npm start
```

By default, the application will run on port `8090`.

| Command | Description
|---------|------------
| `npm start` (Default) | Serve the raw development bundles via http://localhost:8090.
| `npm compile` | Output raw development bundles in local /build directory.

## Examples

The examples includes several variants so that you can see how to mix and match individual components and the impact this can have on the resulting bundle size.

### Fetch

This example shows how to use the Fetch Instrumentation with the console exporter and with the B3 Propagator.

Included Components

- FetchInstrumentation
- ZoneContextManager
- WebTracerProvider
- B3Propagator

To see the results, run Deno with `deno run --location=http://localhost:8090 http://localhost:8090/fetch/index.js`. The application is using the `ConsoleSpanExporter` and will post the created spans to the standard output.

## Useful links

- For more information on OpenTelemetry, visit: <https://opentelemetry.io/>
- For more information on web tracing, visit: <https://github.com/open-telemetry/opentelemetry-js/tree/main/packages/opentelemetry-sdk-trace-web>
- For more information on Deno, visit: <https://deno.land/manual>

## LICENSE

Apache License 2.0
