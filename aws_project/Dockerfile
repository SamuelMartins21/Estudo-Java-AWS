FROM eclipse-temurin:20-jdk
VOLUME /tmp
ARG JAR_FILE
COPY target/*.jar app.jar
ARG DEPENDENCY=target/dependency
COPY ${DEPENDENCY}/BOOT-INF/lib /app/lib
COPY ${DEPENDENCY}/META-INF /app/META-INF
COPY ${DEPENDENCY}/BOOT-INF/classes /app
ENTRYPOINT ["java","-jar","/app.jar"]