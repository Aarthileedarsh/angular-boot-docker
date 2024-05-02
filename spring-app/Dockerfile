FROM openjdk:8-alpine

#  docker build -t trion/spring-app .
# docker run --rm -it trion/spring-app
VOLUME /tmp

ENV SPRING_APPLICATION_JSON=\
'{"sample": {"greeting": "Hello from docker!" }}'

EXPOSE 8080


CMD ["java","-XX:+UnlockExperimentalVMOptions","-XX:+UseCGroupMemoryLimitForHeap","-XX:MaxRAMFraction=1","-Djava.security.egd=file:/dev/./urandom","-jar","/app/app.jar"]

#remote debugging
#CMD ["java","-agentlib:jdwp=transport=dt_socket,server=y,suspend=n,address=9009","-Djava.security.egd=file:/dev/./urandom","-jar","/app/app.jar"]

#debugging, wait for debugger
#CMD ["java","-agentlib:jdwp=transport=dt_socket,server=y,suspend=y,address=9009","-Djava.security.egd=file:/dev/./urandom","-jar","/app/app.jar"]
