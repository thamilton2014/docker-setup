Docker infrastructure for automation
===

### Building the images

Browsermob

```bash
docker build -t docker/browsermob docker-browsermob/
```

Jenkins

```bash
docker build -t docker/jenkins docker-jenkins/
```

Jenkins Ruby Slave

```bash
docker build -t jenkins/node-ruby docker-jenkins-ruby/
```

Selenium Chrome Node

```bash
docker build -t selenium/node-chrome docker-selenium/NodeChrome/
```

Selenium Firefox Node

```bash
docker build -t selenium/node-firefox docker-selenium/NodeFirefox
```

Elasticsearch

```bash
docker build -t docker/elasticsearch elasticsearch/$version/
```

Kibana

```bash
docker build -t docker/kibana kibana/$version
```

Logstash

```bash
docker build -t docker/logstash logstash/$version
```

Redis

```bash
docker build -t docker/redis redis/3.0/
```

## Helpful commands

Update all submodules

```bash
git submodule foreach --recursive git pull origin master
```

Delete all containers

```bash
docker rm -f $(docker ps -a -q)
```

Delete all images

```bash
docker rmi $(docker images -q)
```