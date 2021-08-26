FROM maven:3.5.2-jdk-8-alpine
COPY pom.xml /build/
COPY src /build/src/
COPY mvnw /build/mvnw

WORKDIR /build/
EXPOSE 8080
ENTRYPOINT [ "mvn spring-boot:run"]
