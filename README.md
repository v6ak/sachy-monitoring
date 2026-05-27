## What we use

* Kamon - A monitoring toolkit for applications running on the JVM, providing metrics collection and visualization. It can exports the data to many databases, including InfluxDB.
* InfluxDB - A time-series database designed for high-performance handling of metrics and events. We could use it for monitoring directly, but it seems to be quite ham-fisted, so we use Grafana for it.
* Grafana - A powerful open-source platform for monitoring and observability, enabling the creation of interactive dashboards. We currently use self-hosted instance.

## What we don't use (yet)

* Prometheus – Lila seems to use Prometheus alongside InfluxDB, but I don't know why.

