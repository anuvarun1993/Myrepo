# Stage 1: Build React app
FROM node:20.17.0 AS build

WORKDIR /app
COPY package*.json ./
RUN npm install
COPY . .
RUN npm run build

# Stage 2: Serve with NGINX
FROM nginx:stable-alpine

# Copy React build to NGINX's default public folder
COPY --from=build /app/build /usr/share/nginx/html

# Optional: custom NGINX config
# COPY nginx.conf /etc/nginx/nginx.conf

EXPOSE 80
CMD ["nginx", "-g", "daemon off;"]

