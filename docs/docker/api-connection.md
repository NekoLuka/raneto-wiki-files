## Where is the docker API socket located

The docker Unix socket is located at `/var/run/docker.sock`.
You need a library in your program to connect to the socket.