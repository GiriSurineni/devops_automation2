FROM node:20-alpine

WORKDIR /Giri/app/

COPY package.json .
COPY nicejob.js .

RUN npm install

EXPOSE 5000

ENTRYPOINT ["node", "nicejob.js"]