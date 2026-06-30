FROM nginx:alpine

WORKDIR /usr/share/nginx/html

COPY . . 

ENV APP_MODE=production \
    APP_PORT=8080   

LABEL org.opencontainers.image.author="hamza" \
    org.opencontainers.image.description="frontend" \
    org.opencontainers.image.version="1.0"

EXPOSE 80

CMD ["nginx", "-g", "daemon off;"] 
