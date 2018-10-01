# odind-docker

Easily provision [odind](https://odinblockchain.org/) using [Docker](https://www.docker.com/)

## Note
```
Install docker ce (Community edition).
OS is specified inside the docker file so there is no specific OS requirements.

## Quickstart from Docker Hub
```
docker run --rm -d -v ~/odin-wallet/:/root/.odin/ --name=odind-docker odinblockchain/odind-docker
```

## Docker build and run from source
```
docker build -t odind-docker .
docker run --rm -d -v ~/odin-wallet/:/root/.odin/ --name=odind-docker odind-docker
```

## Staking
```
docker exec odind-docker odin-cli getnewaddress
docker exec odind-docker odin-cli encryptwallet "yoursecretpass"
docker exec odind-docker odin-cli walletpassphrase "yoursecretpass" 9999999999 true
docker exec odind-docker odin-cli getstakingstatus
```
## Tips
```
docker exec -i -t odind-docker /bin/bash - This will open a session inside the container where you can work.

## Masternode:
```
Still to come.
