FROM openjdk:8-jdk-slim
ARG MAVEN_VERSION=3.8.2
RUN apt-get update
RUN mkdir /build
WORKDIR /build
COPY pom.xml /build
COPY src /build/src
COPY mvnw /build
COPY mvnw.cmd /build
#RUN apt install maven
#RUN mvn dependency:go-offline -B
RUN mvn package
#COPY target /build/target
EXPOSE 8080
CMD [ "mvn spring-boot:run"]
