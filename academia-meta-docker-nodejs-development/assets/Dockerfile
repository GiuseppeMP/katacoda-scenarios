FROM node:alpine

COPY package.json .

RUN npm install

COPY . .

ENTRYPOINT npm start