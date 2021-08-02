FROM adoptopenjdk/openjdk11
ADD ./target/order-gatway-1.0-SNAPSHOT.jar /orderGateway.jar
ADD ./run.sh /run.sh
RUN chmod a+x /run.sh
EXPOSE 8085:8085
CMD /run.sh
