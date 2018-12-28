# Use a lighter version of Node as a parent image
FROM mhart/alpine-node:10

# Set the working dir to /client
WORKDIR /client

# copoy package.json into the container at /client
COPY package*.json /client/

# install deps
RUN npm install
RUN npm install -g @angular/cli@1.7.1

# COPY the current directory contents
COPY . /client/

# expose port 4200
EXPOSE 4200

# Run the app when the container launches
CMD ng serve --host 0.0.0.0
