# Pulling Ubuntu image
FROM ubuntu:20.04

# Updating packages
RUN apt-get update 

# Execute tail command with -f flag
ENTRYPOINT ["tail", "-f", "/var/log/hello.log"]
