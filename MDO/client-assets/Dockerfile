FROM node:16

WORKDIR /usr/src/app

COPY . .
RUN sed -i 's/stretch/buster/' /etc/apt/sources.list && apt update && apt install -y zip && apt-get install -y libjpeg-turbo-progs nasm
RUN npm install && npm run build

RUN zip -r dist.zip dist
