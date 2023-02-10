FROM alpine

# Install the cmatrix package
RUN apk add --no-cache cmatrix

# Set the default command
CMD ["cmatrix", "-a"]

# Allocate a TTY and keep stdin open
ENTRYPOINT ["/bin/sh", "-c", "exec cmatrix -a < /dev/tty"]
