FROM    maven:3-openjdk-11
RUN     mkdir /build
WORKDIR  /build
COPY    src /build/src
COPY    pom.xml .
CMD     ["mvn","-c","spring-boot:run"]