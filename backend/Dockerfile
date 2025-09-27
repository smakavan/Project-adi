FROM openjdk:8
WORKDIR /app
COPY target/backend-1.0-RELEASE.jar app.jar
EXPOSE 8081
ENTRYPOINT ["java","-jar","app.jar"]
