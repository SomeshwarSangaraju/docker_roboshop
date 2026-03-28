FROM python:3.10-alpine3.22
RUN apk add --no-cache \
    gcc \
    g++ \
    musl-dev \
    libffi-dev \
    openssl-dev \
    python3-dev \
    linux-headers \
    make \
    curl
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