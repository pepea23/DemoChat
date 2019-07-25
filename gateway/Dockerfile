FROM node:10.15-alpine

WORKDIR /app

RUN apk add --update-cache python make g++ curl

COPY package.json .
COPY yarn.lock .
COPY server.js .

RUN yarn install

EXPOSE 3010

ENTRYPOINT ["sh","-c", "node server.js"]


