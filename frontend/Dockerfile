# Use a lightweight Nginx base image.
FROM nginx:alpine

# Copy the custom Nginx configuration file into the container.
COPY nginx.conf /etc/nginx/conf.d/default.conf

# Copy all the frontend files (HTML, JS, CSS, etc.) into the Nginx public directory.
COPY . /usr/share/nginx/html

# Expose the port 
EXPOSE 80

CMD ["nginx", "-g", "daemon off;"]