# Etapa 1: Construcción
FROM maven:3.9.5-eclipse-temurin-21 AS build
WORKDIR /app

COPY pom.xml ./
COPY src ./src

RUN --mount=type=cache,target=/root/.m2 mvn clean package -DskipTests

# Etapa 2: Ejecución
FROM eclipse-temurin:21-jre-alpine
WORKDIR /app

COPY --from=build /app/target/*.jar app.jar

EXPOSE 8080

CMD ["java", "-jar", "app.jar"]