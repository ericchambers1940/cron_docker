# Pulling Ubuntu image
FROM ubuntu:20.04

# Updating packages
RUN apt-get update -y && apt-get install openssh-server -y

# Create cron logfile
RUN touch /var/log/hello.log

# Execute tail command with -f flag
ENTRYPOINT ["tail", "-f", "/var/log/hello.log"]
