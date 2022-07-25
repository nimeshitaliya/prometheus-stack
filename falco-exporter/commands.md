## References 
- https://github.com/falcosecurity/charts/tree/master/falco-exporter

## Prerequisite to create deploy falco-exporter
- Before using this chart, you need Falco installed and running with the gRPC Output enabled (over Unix socket by default).
- Enabled deployment of a Prometheus operator Service Monitor.
- To configure prometheus opertator to pick falco exporter as a target need to set `prometheus.prometheusSpec.serviceMonitorSelectorNilUsesHelmValues: false`

### Create service monitor in ivari-sandbox-values.yaml for falco exporter to connect with Prometheus operator
```yaml
serviceMonitor:
  enabled: true
```
