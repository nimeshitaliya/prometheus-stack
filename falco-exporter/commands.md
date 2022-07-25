## References 
- https://github.com/falcosecurity/charts/tree/master/falco-exporter

## Prerequisite to create deploy locust
- Before using this chart, you need Falco installed and running with the gRPC Output enabled (over Unix socket by default).
- Enabled deployment of a Prometheus operator Service Monitor.
- To configure prometheus opertator to pick falco exporter as a target need to set `prometheus.prometheusSpec.serviceMonitorSelectorNilUsesHelmValues: false`

### Enable HPA on locust worker nodes in ivari-sandbox-values.yaml
```yaml
serviceMonitor:
  enabled: true
```
