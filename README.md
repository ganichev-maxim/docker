docker run -p 3000:3000 -d --name grafana grafana/grafana-enterprise
docker stats grafana
docker logs grafana > log.txt
docker exec grafana env > env.txt
docker exec -it grafana grafana cli admin reset-admin-password ****
docker exec -it grafana curl -s -u admin:admin http://localhost:3000/api/users
