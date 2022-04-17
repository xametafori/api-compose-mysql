FROM openjdk:8-jdk-alpine
RUN addgroup -S devopsc && adduser -S javams -G devopsc
USER javams:devopsc
ENV JAVA_OPTS=""
ARG JAR_FILE
ADD ${JAR_FILE} api-man-socios-mysql.jar
 # use a volume is mor efficient and speed that filesystem
VOLUME /tmp
EXPOSE 8096
ENTRYPOINT [ "sh", "-c", "java $JAVA_OPTS -Djava.security.egd=file:/dev/./urandom -jar /api-man-socios-mysql.jar" ]

