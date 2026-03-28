FROM python:3.10-alpine3.22
WORKDIR /opt
COPY *.py .
COPY *.ini .
COPY *.txt .
RUN pip3 install -r requirements.txt
ENV CART_HOST="cart"
ENV CART_PORT="8080"
ENV USER_HOST="user"
ENV USER_PORT="8080"
ENV AMQP_HOST="rabbitmq"
ENV AMQP_USER="roboshop"
ENV AMQP_PASS="roboshop123"
CMD ["uwsgi", "--ini", "payment.ini"]