FROM  openjdk:8-jdk
LABEL MAINTAINER ruoyi

ENV PARAMS=" --server.port=8080 --springprofiles.active=prod --spring.cloud.nacos.server-addr=nacos.common"

COPY target/*.jar /app.jar
EXPOSE 8080

ENTRYPOINT ["/bin/sh","-c","java  -Dfile.encoding=urf8 -Djava.security.egd=file:/dev/./urandom","-jar","/app.jar" ,"${PARAMS}"]
