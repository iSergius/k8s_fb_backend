FROM adoptopenjdk/openjdk14:ubi

ENV THE_APP_JAR mconveyor-manager-srv-0.0.1-SNAPSHOT.jar
ENV THE_APP_JAR_PATH jars/$THE_APP_JAR

RUN mkdir /opt/app
COPY $THE_APP_JAR_PATH /opt/app
CMD ["sh", "-c", "java -jar -Dspring.profiles.active=local,local-docker /opt/app/$THE_APP_JAR"]

#EXPOSE ${EXPOSED_PORT} 9000

LABEL "project"="ubrr_mconveyor"
