# 🐳 Teste cappta DevOps A/B

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
for i in `seq 1 100`; do curl http://localhost; done

# esperado
legado
novo c546b64238cc
legado
legado
novo fde88d31666c
legado
legado
legado
legado
legado
legado
novo c546b64238cc
legado
legado
novo fde88d31666c
legado
...
```