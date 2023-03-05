FROM nginx:latest

RUN mkdir "certs"
RUN openssl dhparam --dsaparam -out /certs/dhparam.pem 4096

COPY nginx.conf /etc/nginx/nginx.conf
COPY cert-info.conf /etc/nginx/ssl/cert-info.conf
COPY ssl-params.conf /etc/nginx/ssl/ssl-params.conf