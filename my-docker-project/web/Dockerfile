# web/Dockerfile
FROM nginx:latest

RUN rm /etc/nginx/conf.d/default.conf

COPY config/default.conf /etc/nginx/conf.d/default.conf

COPY html/ /usr/share/nginx/html/

EXPOSE 80

CMD ["nginx", "-g", "daemon off;"]
