FROM node:alpine
#RUN  apt update && apt npm install
RUN mkdir /app
WORKDIR /app
COPY package.json /app
COPY . /app
RUN npm install
RUN npm start
