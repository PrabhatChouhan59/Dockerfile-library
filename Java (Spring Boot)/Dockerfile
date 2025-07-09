# Use Eclipse Temurin JDK for Java 17
FROM eclipse-temurin:17-jre-alpine

# Copy the built JAR file into the container
COPY target/myapp.jar /app/app.jar

# Expose the default Spring Boot port
EXPOSE 8080

# Run the Spring Boot application
CMD ["java", "-jar", "/app/app.jar"]
