FROM maven:3.5.2-jdk-8-alpine 
COPY pom.xml /build/
RUN mvn  install
COPY src /build/src/
COPY mvnw /build/
COPY mvnw.cmd /build/ 
#COPY target /build/target
WORKDIR /build/
EXPOSE 8080
CMD [ "mvn spring-boot:run"]
