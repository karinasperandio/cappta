# Alpine como alternativa leve
# @see https://hub.docker.com/_/nginx/
# docker build --platform=linux . -t cappta/novo
# docker run -d -p 81:80 cappta/novo
FROM nginx:alpine
CMD echo "novo $HOSTNAME" > /usr/share/nginx/html/index.html;nginx -g 'daemon off;'
