# Use the official lightweight Nginx image
FROM nginx:alpine

# Copy custom Nginx configuration into the container
COPY ./nginx.conf /etc/nginx/nginx.conf

# Expose port 80 for HTTP traffic
EXPOSE 80

# Run Nginx in the foreground (required for Docker)
CMD ["nginx", "-g", "daemon off;"]
