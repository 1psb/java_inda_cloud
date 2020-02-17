FROM openjdk:8-jdk-alpine
VOLUME /tmp
EXPOSE 8082
EXPOSE 5082
ENV JAVA_OPTS="-Xmx128m -Dfile.encoding=UTF-8 -agentlib:jdwp=transport=dt_socket,address=5082,server=y,suspend=n"
ADD target/po-0.0.1-SNAPSHOT.jar app.jar
ENTRYPOINT exec java $JAVA_OPTS -Djava.security.egd=file:/dev/./urandom -jar /app.jar
