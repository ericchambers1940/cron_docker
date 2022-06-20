# cron_docker repo
A repository containing files for tinkering with running cronjobs which executes commands to another container.

# Usage
- Create Docker network, enabling both containers to communicate over port 22:
`docker network create test-network`
- Build Docker Image configured to run cron (run from Dockerfile directory): `docker build Dockerfile.cron`
- Copy image id to clipboard: `docker image ls`
- Run first container in the background: `docker run -d -p 22 --name c1 --network test-network imageidhere`
