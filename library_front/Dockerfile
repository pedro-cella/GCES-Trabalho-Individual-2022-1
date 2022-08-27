FROM node:16.17.0

RUN mkdir /library_front

WORKDIR /library_front

COPY package.json /library_front/

RUN npm install

COPY . .