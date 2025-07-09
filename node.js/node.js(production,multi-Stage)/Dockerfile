# Stage 1: Build the application
FROM node:20 AS build
WORKDIR /app
COPY package*.json ./
RUN npm ci
COPY . .
RUN npm run build

# Stage 2: Create a lightweight production image
FROM node:20-alpine
WORKDIR /app

# Copy the built application from the previous stage
COPY --from=build /app/dist ./dist
COPY package*.json ./

# Install only production dependencies
RUN npm ci --only=production
EXPOSE 3000

# Run the production server
CMD ["node", "dist/server.js"]
