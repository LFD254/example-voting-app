FROM maven:3.5-jdk-8-alpine as build
WORKDIR /code
COPY . .
RUN mvn package -D skipTestso

FROM openjdk:8-jre-alpine as run
COPY --from=build code/target/worker-jar-with-dependencies.jar target/worker-jar-with-dependencies.jar
CMD ["java", "-jar", "target/worker-jar-with-dependencies.jar"]
