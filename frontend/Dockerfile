# Use OpenJDK 8 as base image
FROM openjdk:8

# Set working directory inside container
WORKDIR /app

# Create required directories (optional if your JAR already contains resources)
RUN mkdir -p src/main/webapp/resources target

# Copy frontend resources and JAR
COPY src/main/webapp/* /app/src/main/webapp/
COPY target/frontend-1.0-RELEASE.jar /app/target/frontend.jar

# Expose the port your app will run on
EXPOSE 8085

# Use environment variable BACKEND for dynamic backend URL
# Resolve the variable at runtime using sh -c
CMD ["sh", "-c", "java -Dapi.host.baseurl=${BACKEND} -jar target/frontend.jar"]
