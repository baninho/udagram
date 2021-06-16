# Use NodeJS base image
FROM node:12

# Create app directory in Docker
WORKDIR /usr/app

# Install app dependencies by copying
# package.json and package-lock.json
COPY package*.json ./

# Install dependencies in Docker
RUN npm install -g ionic
RUN npm install

# Copy app from local environment into the Docker image
COPY . .

# Build frontend app
RUN ionic build

# Set the frontend port number
EXPOSE 8100

# Define Docker’s behavior when the image is run
CMD ionic serve --external
