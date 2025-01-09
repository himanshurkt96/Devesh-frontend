
FROM nginx:latest

RUN rm -rf /usr/share/nginx/html/*

COPY . /usr/share/nginx/html/

COPY nginx.conf /etc/nginx/nginx.conf


RUN mkdir -p /etc/nginx/ssl

COPY /etc/letsencrypt/live/deveshnair.com/fullchain.pem /etc/nginx/ssl/fullchain.pem
COPY /etc/letsencrypt/live/deveshnair.com/privkey.pem /etc/nginx/ssl/privkey.pem


EXPOSE 80 443

CMD ["nginx", "-g", "daemon off;"]
