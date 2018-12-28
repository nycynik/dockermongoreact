# Use a lighter version of Node as a parent image
FROM mhart/alpine-node:10

# Set the working dir to /client
WORKDIR /client

# copoy package.json into the container at /client
COPY package*.json /client/

# install deps
RUN npm install

# COPY the current directory contents
COPY . /client/

# expose port 3000
EXPOSE 3000

# Run the app when the container launches
CMD ["npm", "start"]
