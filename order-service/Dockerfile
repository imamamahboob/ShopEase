FROM maven:3.8.1-openjdk-11 AS build
WORKDIR /app
COPY . /app
RUN mvn clean package
FROM openjdk:11-jre-slim
WORKDIR /app
COPY --from=build /app/target/orderservice-0.0.1-SNAPSHOT.jar /app/orderservice.jar
CMD ["java", "-jar", "/app/orderservice.jar"]

