---
Title: How volumes work in swarm mode
---

## How volumes work in swarm mode

When you have multiple services with a volume, all services use the same
volume at the same time. That way changes are immidiatly propegated to
all the services that are running that are using that volume.