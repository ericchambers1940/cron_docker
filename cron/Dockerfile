# Pulling Ubuntu image
FROM ubuntu:20.04

# Updating packages and installing cron
RUN apt-get update && apt-get install cron -y && apt-get install openssh-client -y 

# Adding crontab to the appropriate location
ADD hello-cron /etc/cron.d/hello-cron

# Giving permission to crontab file
RUN chmod 0644 /etc/cron.d/hello-cron

# Running crontab
RUN crontab /etc/cron.d/hello-cron

# Creating entry point for cron 
ENTRYPOINT ["cron", "-f"]
