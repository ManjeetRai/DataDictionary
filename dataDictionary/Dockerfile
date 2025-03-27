# Use a lightweight Java 17 runtime base image
FROM eclipse-temurin:17-jdk-alpine

# Create a working directory
WORKDIR /app

# Copy the packaged jar file into the container
# Make sure to build your project first with: mvn clean install
COPY target/dataDictionary-0.0.1-SNAPSHOT.jar app.jar

# Expose port 8080 (default for Spring Boot)
EXPOSE 8080

# Run the jar file
ENTRYPOINT ["java", "-jar", "app.jar"]
