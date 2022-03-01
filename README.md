# Tpswarm
Executer les images : 
docker-compose -f wordpress-compose.yml up -d
docker-compose -f traefik-compose.yml up -d

Créer des configs local :
docker network create wp-traefik

lancer les stacks :
docker stack deploy --compose-file traefik-compose.yml Tpswarm
docker stack deploy --compose-file wordpress-stack.yml Tpswarm

Log acme :
docker logs -f CONTAINER_ID