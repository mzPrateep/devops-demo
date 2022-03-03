# base image
FROM node:alpine

# set working directory
WORKDIR /app

# add `/usr/src/app/node_modules/.bin` to $PATH
COPY package.json ./

COPY package-lock.json ./

# install and cache app dependencies
RUN npm install
EXPOSE 3000
COPY . ./
# start app
CMD ["npm", "start"]
