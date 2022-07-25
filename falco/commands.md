## References 
- https://github.com/falcosecurity/charts/tree/master/falco

## Prerequisite to create deploy falco
- By default the gRPC server is off.
- We have to enable local unix socket with no authentication to connect with exporter.
- Enable the gRPC output and events will be kept in memory until you read them with a gRPC client.

### Enable falco grpc in ivari-sandbox-values.yaml
```yaml
falco:
  grpc:
    enabled: true
  grpcOutput:
    enabled: true
```
