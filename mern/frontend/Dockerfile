# Use the official image as a parent image
FROM node:18.9.1

# Set the working directory
WORKDIR /app

# copy in package list into WORKDIR (/app)
# COPY package.json package-lock.json .

# Copy the file from your host to your current location
COPY package.json .

# install packages
# RUN npm ci && npm cache clean --force

# Run the command inside your image filesystem
RUN npm install

# Inform Docker that the container is listening on the specified port at runtime
EXPOSE 5713

# Copy the rest of your app's source code from your host to your image filesystem
COPY . .

# Run the specified command within the container
CMD ["npm", "run", "dev"]

