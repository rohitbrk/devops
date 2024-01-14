# official Node.js image as a base
FROM node:16-alpine

# create a working directory within the container
WORKDIR /app

# copy package.json and package-lock.json files to the container
COPY package*.json ./

# install dependencies
RUN npm install

# copy the rest of the app's files to the container
COPY . .

# expose the port the app will run on 
EXPOSE 3000

# start the app
CMD ["node", "index.js"]
