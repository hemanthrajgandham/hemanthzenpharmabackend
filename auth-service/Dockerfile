FROM eclipse-temurin:17-jre
ARG UID=1000
ARG GID=1000
RUN groupadd -g $GID pharma & useradd -g $GID -u $UID -m pharma
WORKDIR /app
RUN groupadd -r pharma && useradd -r -g pharma pharma
COPY target/*.jar app.jar
USER pharma
EXPOSE 8081
ENTRYPOINT ["java", "-jar", "-Djava.security.egd=file:/dev/./urandom", "app.jar"]


