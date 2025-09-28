FROM openjdk:8

# Set working directory
WORKDIR /app

# Copy backend JAR
COPY target/backend-1.0-RELEASE.jar /app/backend.jar

# Expose the backend port
EXPOSE 8080

# Run the JAR and allow environment variables for configuration
CMD ["sh", "-c", "java -Dserver.port=${BACKEND_PORT:-8080} -Ddb.host=${DB_HOST} -Ddb.port=${DB_PORT} -jar /app/backend.jar"]
