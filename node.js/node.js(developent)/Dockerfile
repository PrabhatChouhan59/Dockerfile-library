# Use the official Node.js image, version 20
FROM node:20

# Set the working directory inside the container
WORKDIR /app

# Copy package.json and package-lock.json for dependency installation
COPY package*.json ./

# Install dependencies
RUN npm install

# Copy all remaining source code to the working directory
COPY . .

# Expose port 3000 (commonly used by Node.js apps)
EXPOSE 3000

# Start the application using npm
CMD ["npm", "start"]
