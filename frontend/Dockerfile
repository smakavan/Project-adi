FROM openjdk:8
WORKDIR /app
COPY target/frontend-1.0-RELEASE.jar app.jar
EXPOSE 8080
ENTRYPOINT ["java","-jar","app.jar"]
