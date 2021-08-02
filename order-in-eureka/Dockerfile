FROM adoptopenjdk/openjdk11
VOLUME /tmp
ADD target/order-in-eureka-1.0-SNAPSHOT.jar app.jar
ENTRYPOINT ["java","-jar","app.jar"]
EXPOSE 8761