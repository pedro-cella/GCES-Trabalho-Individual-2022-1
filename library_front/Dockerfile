FROM node:16.17.0 as build-stage

RUN mkdir /library_front

WORKDIR /library_front

COPY package.json /library_front/

RUN npm install

COPY . .

RUN npm run build

FROM nginx:latest

COPY --from=build-stage /library_front/build /usr/share/nginx/html

COPY ./nginx/nginx.conf /etc/nginx/conf.d/default.conf

EXPOSE 3000