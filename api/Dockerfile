# Use a lighter version of Node as a parent image
FROM mhart/alpine-node:10

# Set the working dir to /client
WORKDIR /api

# copoy package.json into the container at /client
COPY package*.json /api/

# install deps
RUN npm install

# COPY the current directory contents
COPY . /api/

# expose port 3000
EXPOSE 3000

# Run the app when the container launches
CMD ["npm", "start"]

