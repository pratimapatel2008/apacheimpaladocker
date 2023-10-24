# apacheimpaladocker

1. Create Docker Network
```
docker network create -d bridge quickstart-network
```
2. Set Quick start network.
```
export QUICKSTART_IP=$(docker network inspect quickstart-network -f '{{(index .IPAM.Config 0).Gateway}}')
export QUICKSTART_LISTEN_ADDR=0.0.0.0
```
3. Clone Git repository and switch directory
```
git clone https://github.com/pratimapatel2008/apacheimpaladocker.git && cd apacheimpaladocker
```
4. Start Impala service
```
docker-compose -f quickstart.yml up -d
```
4. Stop
```
docker-compose -f quickstart.yml down
```
