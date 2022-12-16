# syntax=docker/dockerfile:1
FROM node:16

#To improve performance
ENV NODE_ENV=production
#Create app directory
WORKDIR /usr/src/app

#Install app dependencies
# A wildcard is used to ensure both package.json and package-lock.json are copied

COPY package*.json ./

RUN npm ci --only=production

#Bundle app source
COPY . .

EXPOSE 8080

CMD [ "node", "server/index.js" ]
