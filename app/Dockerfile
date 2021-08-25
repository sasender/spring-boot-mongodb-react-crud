FROM node:10-alpine as build-
RUN  apt update && apt npm install
RUN mkdir /app
WORKDIR /app
COPY package.json /app
RUN npm install
COPY . /app
RUN npm start
