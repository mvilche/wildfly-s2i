# Wildfly S2i images - Linux Alpine

![Docker Stars](https://img.shields.io/docker/stars/mvilche/wildfly-s2i.svg)
![Docker Pulls](https://img.shields.io/docker/pulls/mvilche/wildfly-s2i.svg)
![Docker Automated](https://img.shields.io/docker/cloud/automated/mvilche/wildfly-s2i)
![Docker Build](https://img.shields.io/docker/cloud/build/mvilche/wildfly-s2i)


# Features

- Non-root
- Okd ready!
- Kubernetes ready!
- Jolokia Agent JMX Metrics
- Prometheus JMX Exporter Metrics
- Maven 3.8.4
- OpenJdk and OpenJre images
- Openjdk 11 y 8 Support


### Deploy Environment Variables 


| Variable | Details |
| ------ | ------ |
| TIMEZONE | Set Timezone (America/Montevideo, America/El_salvador) |
| WAITFOR_HOST | set name host |
| WAITFOR_PORT | set port for WAITFOR_HOST |
| JOLOKIA_ENABLE | Enable jolokia jmx monitoring - Values: 1 (Enable), 0 (Disable - default value)|
| PROMETHEUS_ENABLE | Enable prometheus jmx monitoring - Values: 1 (Enable), 0 (Disable - default value)|
| EXTRA_JAVA_OPTS | Add options to default JAVA_OPTS options |
| JAVA_OPTS | Override JAVA_OPTS options |



### Build Environment Variables 

| Variable | Details |
| ------ | ------ |
| MVN_OPTS | Maven options |
| MVN_OVERRIDE_COMMAND | Override default maven command |
| NEXUS_MIRROR_URL | Nexus repository override repository in pom.xml |




### Generate builder image

```console

Example build Wildfly 25 jdk 11

 docker build -t wildfly-s2i:25-jdk11 -f 25/Dockerfile.jdk11 contrib

```

### Wildfly application image use s2i

```console

Example build app using Wildfly 25 builder image

s2i build https://github.com/myuser/sample-app.git wildfly-s2i:25-jdk11 myapp:latest --incremental

```


### Run application

```console

docker run -p 8080:8080 myapp:latest

```

### How use s2i

```console

https://github.com/openshift/source-to-image

```




License
----

Martin vilche
