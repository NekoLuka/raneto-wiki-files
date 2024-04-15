---
Title: JWT Certificate Manager
---

# JWT Certificate Manager
A simple tool that can be eiter run as a CLI tool or as a webserver.
Manage your keypairs to generate JWT's with a single (offline) source of truth.

## Ideas
- Example of how to proxy to server over SSH to not publicly run webserver
- Default run webserver on localhost (with big warning when running on anything but localhost)
- Private keys never leave server and are not visible in either CLI or webserver

## Features
- Run as a CLI
- Run as a webserver
- Sqlite DB encrypted with symmetrical encryption
