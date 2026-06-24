FROM eclipse-temurin:17-jre
ARG UID=1000
ARG GID=1000
RUN groupadd -g $GID pharma && \
    useradd -u $UID -g pharma -m pharma
WORKDIR /app
COPY target/*.jar app.jar
USER pharma
EXPOSE 8081
ENTRYPOINT ["java", "-jar", "-Djava.security.egd=file:/dev/./urandom", "app.jar"]


