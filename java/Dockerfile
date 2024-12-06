FROM maven:3.9.9-eclipse-temurin-8 AS builder

WORKDIR /app

COPY . .

RUN mvn clean package -DskipTests

FROM eclipse-temurin:8-jre

WORKDIR /app

LABEL maintainer="Séraphin"

COPY --from=builder /app/target/java-0.0.1-SNAPSHOT.jar app.jar


EXPOSE 8448

CMD ["java", "-jar", "app.jar"]