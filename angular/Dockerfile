FROM nginx:1.27-alpine

COPY nginx/ /etc/nginx

COPY e2e/ /usr/share/nginx/html

COPY entrypoint.sh /dockerfile.entrypoint.d/entrypoint.sh