FROM  openjdk:8-jdk-alpine
LABEL MAINTAINER RexYu

ENV PARAMS=" --server.port=8080 --spring.profiles.active=prod --spring.cloud.nacos.server-addr=nacos.common:8848  --spring.cloud.nacos.discovery.server-addr=nacos.common:8848 --spring.cloud.nacos.config.server-addr=nacos.common:8848 --spring.cloud.nacos.discovery.namespace=prod --spring.cloud.nacos.config.namespace=prod"

COPY target/*.jar /app.jar
EXPOSE 8080

ENTRYPOINT ["/bin/sh","-c","java  -Dfile.encoding=urf8 -Djava.security.egd=file:/dev/./urandom -jar /app.jar ${PARAMS}"]
