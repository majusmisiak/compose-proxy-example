# compose-proxy-example

See [stackoverflow](https://stackoverflow.com/questions/39913757/restrict-internet-access-docker-container?noredirect=1&lq=1).

```bash
# build the docker images
docker-compose build

# run docker compose
docker-compose up

# check http and https
client_container_id=` docker ps | grep client | awk '{ print $1 }' `
docker exec $client_container_id wget http://google.com -O - >/dev/null
docker exec $client_container_id wget https://google.com -O - >/dev/null
```
