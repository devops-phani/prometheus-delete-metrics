# Prometheus-delete-metrics


Delete `node_cpu_seconds_total` metric from prometheus using prometheus admin api.

```
curl -X POST -g 'http://prometheus:9090/api/v1/admin/tsdb/delete_series?match[]=node_cpu_seconds_total'
```

Cleanup the deleted the metrics from disk prometheus admin api.

```
curl -X POST http://prometheus:9090/api/v1/admin/tsdb/clean_tombstones
```

Reference links

- https://prometheus.io/docs/prometheus/latest/querying/api/#delete-series
- https://faun.pub/how-to-drop-and-delete-metrics-in-prometheus-7f5e6911fb33
- https://stackoverflow.com/questions/49859360/how-do-i-delete-a-time-series-from-prometheus-v2-specifically-a-series-of-alert
