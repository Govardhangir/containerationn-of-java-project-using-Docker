# Stage 1: Build
FROM maven:3.9.9-eclipse-temurin-21 AS build_image
RUN apt-get update && apt-get install -y git
RUN git clone https://github.com/hkhcoder/vprofile-project.git
WORKDIR /vprofile-project
RUN git checkout containers && mvn clean package -DskipTests

# Stage 2: Deploy
FROM tomcat:10-jdk21
RUN rm -rf /usr/local/tomcat/webapps/*
COPY --from=build_image /vprofile-project/target/vprofile-v2.war /usr/local/tomcat/webapps/ROOT.war
EXPOSE 8080
CMD ["catalina.sh", "run"]

