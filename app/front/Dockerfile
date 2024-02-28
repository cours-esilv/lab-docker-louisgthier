# Use an official Nginx runtime as a parent image
FROM nginx:alpine

# Set the working directory in the container to /app
WORKDIR /app

# Copy the current directory contents into the container at /app
COPY . /app
COPY index.html /usr/share/nginx/html/index.html

# Make the script executable
RUN chmod +x /app/entrypoint.sh

# Set environment variables
ENV WS_BACK_URL http://mlops-back:5000

# Use entrypoint.sh as entrypoint
ENTRYPOINT ["/app/entrypoint.sh"]

# Expose port 80
EXPOSE 80

# docker build ./app/front --tag mlops-front
# docker network create mlops-network
# docker run --name mlops-front -p 8002:80 -d --network mlops-network mlops-front