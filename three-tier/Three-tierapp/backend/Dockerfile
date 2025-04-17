FROM node:latest

WORKDIR /backend

COPY . .

ENV NODE_OPTIONS=--openssl-legacy-provider
RUN npm install --legacy-peer-deps  

EXPOSE 80
ENV MYSQL_HOST=sql_cont
ENV MYSQL_USER=external_user
ENV MYSQL_PASSWORD=password
ENV MYSQL_DB=test

CMD ["npm" , "start"]

