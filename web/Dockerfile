FROM maven:3.5.2-jdk-8-alpine
COPY pom.xml /build/
COPY src /build/src/
WORKDIR /build/
EXPOSE 8080
RUN mvn package


FROM openjdk:8-jre-alpine
WORKDIR /app
COPY --from=MAVEN_BUILD /build/target/docker-boot-intro-0.1.0.jar /app/
CMD ['mvn spring-boot:run']
ENTRYPOINT ["java", "-jar", "docker-boot-intro-0.1.0.jar"]






