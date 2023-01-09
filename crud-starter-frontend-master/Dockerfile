FROM node:16.18-alpine as builder

WORKDIR /app

COPY . ./

RUN npm i

RUN npm run build

FROM nginx

COPY --from=builder /app/build/. /usr/share/nginx/html