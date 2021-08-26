FROM maven:3.8.1-openjdk-11-slim AS builder
RUN apt-get update
RUN mkdir /build
WORKDIR /build
COPY pom.xml /build
RUN mvn clean -e -B package
COPY src /build/src
COPY mvnw /build
COPY mvnw.cmd /build
#RUN apt install maven
#RUN mvn dependency:go-offline -B
RUN mvn package
#COPY target /build/target
EXPOSE 8080
CMD [ "mvn spring-boot:run"]
FROM openjdk:11-jre-slim
WORKDIR /app
