FROM node:18.19 as builder
LABEL stage=builder
WORKDIR /app/
COPY ./ListRickMortyPagesHTTP/package.json /app/
RUN npm install
COPY ./ListRickMortyPagesHTTP/ /app/
RUN ng build

FROM nginx:latest
COPY --from=builder /app/dist/ListRickMortyPagesHTTP/ /usr/share/nginx/html
EXPOSE 8081