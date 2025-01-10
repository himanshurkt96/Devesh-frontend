FROM nginx:latest

RUN rm -rf /usr/share/nginx/html/*


COPY . /usr/share/nginx/html/


COPY nginx.conf /etc/nginx/nginx.conf


RUN mkdir -p /etc/nginx/ssl


COPY ssl/fullchain.pem /etc/nginx/ssl/fullchain.pem
COPY ssl/privkey.pem /etc/nginx/ssl/privkey.pem


EXPOSE 80 443


CMD ["nginx", "-g", "daemon off;"]
