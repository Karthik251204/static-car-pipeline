# Use nginx image to serve static website
FROM nginx:alpine

# Copy website files to nginx default html directory
COPY . /usr/share/nginx/html

# Expose port 80
EXPOSE 80

# Run nginx in foreground
CMD ["nginx", "-g", "daemon off;"]
