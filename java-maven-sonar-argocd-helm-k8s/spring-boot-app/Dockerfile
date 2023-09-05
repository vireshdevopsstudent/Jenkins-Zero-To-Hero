# You can change this base image to anything else
# But make sure to use the correct version of Java
FROM adoptopenjdk/openjdk11:alpine-jre

# Simply the artifact path
ARG artifact=target/spring-boot-web.jar

WORKDIR /opt/app

COPY ${artifact} app.jar

# This should not be changed
ENTRYPOINT ["java","-jar","app.jar"]

# When the Docker container is started based on this image, it will execute the java -jar app.jar command. Here's what each part does in more detail:

# java: This is the Java Virtual Machine (JVM) executable. It's responsible for running Java applications.

# -jar: This is an argument passed to the java command. It tells the JVM to execute the JAR file specified as the next argument.

# app.jar: This is the JAR file that contains the Spring Boot application code and dependencies. When the java -jar app.jar command is executed, it launches the Spring Boot application contained within this JAR file. The Spring Boot application's main class is defined in the JAR's manifest file, and that main class is executed as the entry point for the application.

# So, in summary, "java","-jar","app.jar" is a command that tells Docker to run a Java application using the Java Virtual Machine (java). It specifies that the application is contained within the app.jar file, and the JVM should execute this JAR file as the entry point for the Docker container.






