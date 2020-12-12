# Wildfly s2i images 

![Docker Stars](https://img.shields.io/docker/stars/mvilche/wildfly-s2i.svg)
![Docker Pulls](https://img.shields.io/docker/pulls/mvilche/wildfly-s2i.svg)
![Docker Automated](https://img.shields.io/docker/cloud/automated/mvilche/wildfly-s2i)
![Docker Build](https://img.shields.io/docker/cloud/build/mvilche/wildfly-s2i)


# Funcionalidades:

- Non-root
- Openshift compatible
- Jolokia Agent
- Jacoco Agent
- Maven
- Mkdocs integration

### Variables


| Variable | Detalle |
| ------ | ------ |
| TIMEZONE | Define la zona horaria a utilizar (America/Montevideo, America/El_salvador) |
| NEXUS_MIRROR_URL | Define url repositorio nexus para la descarga de dependencias |
| EXTRA_REPO | Define url repositorio git extra compila previo |
| MVN_OPTS | Variable usada argumentos adicionales maven |
| MKDOCS_DIR | Directorio donde se encuentra mkdocs.yml - Ejemplo: documentation |
| MKDOCS_CONTEXT_PATH | Nombre del context path donde instalará la documentación. Por defecto es / - Ejemplo: documentation |



### Openshift Install example

oc create -f 21/wildfly-21-s2i-template.yaml

License
----

Martin vilche
