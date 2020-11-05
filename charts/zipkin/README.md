# Open Zipkin

### Ingress configuration example:
```yaml
ui:
  ingress:
    enabled: "true"
    annotations:
      "kubernetes.io/ingress.class": "nginx"
      "nginx.ingress.kubernetes.io/rewrite-target": "/zipkin$1"
    hosts:
      - host: "kubernetes.docker.internal"
        paths:
          - "/zipkin(.*)"
```