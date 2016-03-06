Docker infrastructure for automation
===

Jenkins
###

Start by creating a Jenkins instance

```bash
cd docker-jenkins
docker-compose up -d
```

Install the Jenkins swarm plugin

	- Self-Organizing Swarm Plug-in Modules

Navigate back to the directory and docker-compose the rest of the containers

## Helpful commands

Delete all containers

```bash
docker rm $(docker ps -a -q)
```

Delete all images

```bash
docker rmi $(docker images -q)
```