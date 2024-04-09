## Connect to the docker API from Go

To connect to the docker API socket in Go, you need to give the build in 
HTTP client an connection transporter of type Unix socket.

https://gist.github.com/teknoraver/5ffacb8757330715bcbcc90e6d46ac74 gives instructions on how to do that.