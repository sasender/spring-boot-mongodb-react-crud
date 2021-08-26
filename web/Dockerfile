FROM maven:3.5.2-jdk-8-alpine
COPY pom.xml /build/
COPY src /build/src/
WORKDIR /build/
EXPOSE 8080
CMD ['mvn spring-boot:run']



