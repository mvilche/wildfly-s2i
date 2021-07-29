# Wildfly s2i images 

![Docker Stars](https://img.shields.io/docker/stars/mvilche/wildfly-s2i.svg)
![Docker Pulls](https://img.shields.io/docker/pulls/mvilche/wildfly-s2i.svg)
![Docker Automated](https://img.shields.io/docker/cloud/automated/mvilche/wildfly-s2i)
![Docker Build](https://img.shields.io/docker/cloud/build/mvilche/wildfly-s2i)


# Features

- Non-root
- Openshift ready!
- Jolokia Agent
- Maven

### Variables


| Variable | Detalle |
| ------ | ------ |
| TIMEZONE | Set Timezone (America/Montevideo, America/El_salvador) |
| NEXUS_MIRROR_URL | custom nexus mirror url |
| MVN_OPTS | Custom maven options in build |



### Openshift Install example

oc create -f 21/wildfly-21-s2i-template.yaml

License
----

Martin vilche
