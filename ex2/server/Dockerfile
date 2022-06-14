# Use a Docker base iamage : based on Alpine Linux 
FROM node:alpine

# Create Application Directory 
RUN mkdir -p /usr/src/server

# Set the working directory of the container for all the RUN command 
WORKDIR /usr/src/server

# copy the package.json file which contain all the dependencies required for application 
COPY package.json /usr/src/server

# Install all the dependencies listed in package.json 
RUN npm install 

# Copy all other files from local machine to container
COPY . /usr/src/server 

# Expose container port to the host machine 
EXPOSE 3000

CMD ["node", "server.js"]

