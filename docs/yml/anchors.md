## YAML anchors for reusable snippets

YAML anchors are a way to create reusable snipptes.

### Example

```yaml
version: '3.8'

services:
  raneto:
    image: lscr.io/linuxserver/raneto:latest
    ports:
      - 3000:3000
    volumes:
      - ./config:/config
    deploy: &deployment
      mode: replicated
      replicas: 1
      restart_policy:
        condition: on-failure
        max_attempts: 10
        window: 60s
  uptime-kuma:
    image: louislam/uptime-kuma
    ports:
      - 3001:3001/tcp
    volumes:
      - uptime-kuma:/app/data
    deploy: 
      <<: *deployment
      resources:
        limits:
          memory: 10M
```

### Links
Docker compose example: https://medium.com/@anasanjaria/code-reuse-in-docker-compose-using-yaml-anchor-feature-6cb2ff1d0427