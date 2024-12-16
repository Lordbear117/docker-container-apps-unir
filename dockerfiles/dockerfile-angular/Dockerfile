### STAGE 1: Build ###
FROM node:16-alpine3.18 AS build

WORKDIR /usr/src/app

COPY package.json package-lock.json ./

RUN npm install --frozen-lockfile

COPY . .

RUN npm run build

### STAGE 2: Run ###
FROM nginx:1.26.2-alpine-slim

COPY nginx.conf /etc/nginx/nginx.conf

COPY --from=build /usr/src/app/dist/aston-villa-app /usr/share/nginx/html

EXPOSE 80

CMD ["nginx", "-g", "daemon off;"]
