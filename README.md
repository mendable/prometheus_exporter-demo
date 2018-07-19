# Prometheus Exporter Demo

Demo of the succinct [discourse/prometheus_exporter][prometheus_exporter].

Salient points:

* A ruby daemon periodically generates a gauge value.
* The exporter client in the daemon periodically runs a thread in the background to forward values to the exporter.
* Prometheus (via prometheus.yml) is configured to poll the exporter periodically.
* Grafana is configured to use Prometheus as a datasource (`http://prometheus:9090/`).

## Instructions

1/. Start locally.
```console
user@host:prometheus_expoter-demo$ docker-compose up
```

2/. Visit http://localhost:3000/ and configure Grafana as a datasource.

3/. Create a dashboard with a graph in Grafana to consume the some_value gauge.

[prometheus_exporter]: https://github.com/discourse/prometheus_exporter
