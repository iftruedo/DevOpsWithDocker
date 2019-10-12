FROM ubuntu:16.04
FROM openjdk:8

COPY ./spring-example-project ./spring-example-project/
EXPOSE 8080
WORKDIR ./spring-example-project/
CMD ./mvnw package
RUN ls
CMD ["java","-jar","./target/docker-example-1.1.3.jar"]
