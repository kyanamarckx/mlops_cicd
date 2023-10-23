# Use the official Node.js image version 18.x.x (LTS) as the base image
FROM node:18

# Set the working directory inside the container
WORKDIR /app

# Copy package.json and yarn.lock first and install dependencies
COPY package.json yarn.lock ./
RUN yarn install --frozen-lockfile

# Copy the rest of the application code into the container
COPY . .

# Expose port 3000 for the application to be reachable
EXPOSE 3000

# Command to start the application when the container is started
CMD ["yarn", "start"]
