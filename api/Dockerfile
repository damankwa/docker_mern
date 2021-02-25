# Use a lighter version of Node as a parent image
FROM mhart/alpine-node:8.11.4

# Set the working directory (of the container) to /api
#any RUN, CMD, ENTRYPOINT, COPY and ADD instructions that follow it in the Dockerfile will execute here
# If the WORKDIR doesn’t exist, it will be created
WORKDIR /api

# copy package.json into the container at /api
COPY package*.json /api/

# install dependencies
RUN npm install

# Copy the current directory contents into the container at /api
COPY . /api/

# Make port 80 available to the world outside this container
EXPOSE 9000

# Run the app when the container launches
CMD ["npm", "start"]