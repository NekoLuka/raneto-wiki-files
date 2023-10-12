---
Title: How DNS works in swarm mode
---

## How DNS works in swarm mode

DNS inside of the container overlay network is quite simple.
If there are multiple instances of the same service and there is a request
to that services name, the request will be automatically load-balanced to 
one of the services.