# Alpine como alternativa leve
# @see https://hub.docker.com/_/nginx/
# docker build --platform=linux . -t cappta/proxy-vanilla
# docker run -d -p 80:80 cappta/proxy-vanilla
FROM nginx
ADD nginx.conf /etc/nginx/
