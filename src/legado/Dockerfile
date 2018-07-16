# Nanoserver está sendo utilizado por causa do tamanho da imagem
# @see https://goo.gl/FqdLMR
# docker build --platform=windows . -t cappta/legado
# docker run -d -p 80:80 cappta/legado ping -t localhost
FROM microsoft/iis:nanoserver
RUN echo legado > c:\inetpub\wwwroot\index.html
