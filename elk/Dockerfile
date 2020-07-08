FROM nginx:1.17.6-alpine

COPY server.conf.template /etc/nginx/conf.d/default.conf
COPY ./htpasswd /etc/nginx/
#COPY ./entrypoint.sh /

EXPOSE 80

#RUN chmod +x /entrypoint.sh
#ENTRYPOINT ["/entrypoint.sh"]
#CMD ["nginx", "-g", "daemon off;"]
