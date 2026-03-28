FROM maven:3.9-amazoncorretto-8-alpine
WORKDIR /opt
COPY pom.xml .
COPY src ./src
RUN mvn clean package && \
    mv target/shipping-1.0.jar shipping.jar 
ENV CART_ENDPOINT="cart:8080"
ENV DB_HOST="mysql"
CMD ["java", "-jar", "shipping.jar"]