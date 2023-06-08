# Use a Node.js base image for building the React app
FROM node:14 AS builder

# Set the working directory in the container
WORKDIR /app

# Copy package.json and package-lock.json to the working directory
COPY package*.json ./

# Install dependencies

# Copy the rest of the application code to the working directory
COPY . .

RUN npm install

# Build the React app
RUN npm run build

EXPOSE 3000

# Start the static server to serve the app
CMD ["npm", "start"]
