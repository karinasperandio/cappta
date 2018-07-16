# Teste cappta DevOps

## Construa as imagens

```
docker build --platform=windows src/legado -t cappta/legado
docker build --platform=linux   src/novo   -t cappta/novo
docker build --platform=linux   src/proxy  -t cappta/proxy
```

## Deploy da estrutura

Docker compose:
```
docker-compose -f src/docker-compose.yml -p cappta up
```

## Testando

```
for i in `seq 1 20`; do curl http://localhost; done
ab -n 500 -c 20 http://localhost/
```