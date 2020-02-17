FROM openjdk:8-jdk-alpine
VOLUME /tmp
EXPOSE 8888
EXPOSE 5088
ENV JAVA_OPTS="-Xmx128m -Dfile.encoding=UTF-8 -agentlib:jdwp=transport=dt_socket,address=5088,server=y,suspend=n"
ADD ./config/target/config-0.0.1-SNAPSHOT.jar config/app.jar
ADD ./config-storage config-storage/
ENTRYPOINT exec java $JAVA_OPTS -Djava.security.egd=file:/dev/./urandom -jar config/app.jar
