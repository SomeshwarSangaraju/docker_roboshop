FROM node:20-trixie
WORKDIR /opt
COPY package.json .
COPY *.js .
RUN npm install
ENV REDIS_URL='redis://redis:6379' \
    MONGO="true" \
    MONGO_URL="mongodb://mongodb:27017/users"
CMD ["node", "server.js"]