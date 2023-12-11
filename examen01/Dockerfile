FROM node:20-alpine as angular
WORKDIR /home/app
RUN npm install -g @angular/cli@17
COPY /hello-world/ .
RUN npm ci
RUN ng build

FROM nginx:alpine
WORKDIR /usr/share/nginx/html
RUN rm index.html
COPY --from=angular /home/app/dist/hello-world/browser .
EXPOSE 80