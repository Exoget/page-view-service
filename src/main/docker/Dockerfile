FROM openjdk:8-jdk

EXPOSE 8081

VOLUME /tmp
ADD maven/${project.build.finalName}.jar ${project.build.finalName}.jar
RUN sh -c 'touch /${project.build.finalName}.jar'
ENTRYPOINT ["java","-Djava.security.egd=file:/dev/./urandom","-jar","/${project.build.finalName}.jar"]
