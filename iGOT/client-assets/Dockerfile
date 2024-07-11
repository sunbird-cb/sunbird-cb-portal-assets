FROM node:12

WORKDIR /usr/src/app

COPY . .
RUN sed -i 's/stretch/buster/' /etc/apt/sources.list && apt update && apt install -y zip
RUN rm -rf node_modules
RUN npm install && npm run build

RUN zip -r dist.zip dist
