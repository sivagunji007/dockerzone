FROM maven:3-jdk-11 as MVN
RUN git clone https://github.com/spring-projects/spring-petclinic.git && cd spring-petclinic && mvn package


FROM openjdk:11
LABEL author = "Siva Gunji"
LABEL organization = "Quality Thoughts"
COPY --from=mvn /spring-petclinic/target/spring-petclinic-2.4.2.jar /spring-petclinic-2.4.2.jar
EXPOSE 8080
CMD [ "java", "-jar", "/spring-petclinic-2.4.2.jar" ]