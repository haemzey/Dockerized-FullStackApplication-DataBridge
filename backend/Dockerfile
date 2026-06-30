FROM node:20-alpine

WORKDIR /myapp

COPY package*.json ./

RUN npm ci --only=production  

COPY . . 

LABEL org.opencontainers.image.author="hamza" \
      org.opencontainers.image.description="backend" \
      org.opencontainers.image.version="1.0"

ENV APP_MODE=production \
    APP_PORT=3000 \
    DB_HOST=mysql-db \
    DB_USER=root \
    DB_NAME=appdb 

EXPOSE 3000

CMD ["npm", "start"] 
