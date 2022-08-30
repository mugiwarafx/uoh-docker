# We need java 8
FROM openjdk:8

# This project needs port 8080 to be open
EXPOSE 8080

COPY . .

RUN ./mvnw package

CMD ["java", "-jar", "./target/docker-example-1.1.3.jar"]