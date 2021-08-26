FROM maven:4.0.0-jdk-8-alpine as maven
RUN mkdir /build
WORKDIR /build
COPY pom.xml /build
COPY src /build/src
COPY mvnw /build
COPY mvnw.cmd /build
RUN mvn dependency:go-offline -B
RUN mvn package
#COPY target /build/target
EXPOSE 8080
CMD [ "mvn spring-boot:run"]
