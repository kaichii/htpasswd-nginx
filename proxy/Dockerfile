FROM nginx:latest

ARG USER_NAME
ARG PASSWORD

RUN apt-get update && \
    apt-get install --no-install-recommends -y apache2-utils

RUN htpasswd -Bbn "$USER_NAME" "$PASSWORD" > /etc/nginx/example.htpasswd

COPY nginx.conf /etc/nginx/conf.d/default.conf