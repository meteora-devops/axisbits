FROM nginx:stable

RUN rm -rf /docker-entrypoint.d/10-listen-on-ipv6-by-default.sh
COPY ./nginx.conf /etc/nginx/nginx.conf

WORKDIR /etc/nginx
