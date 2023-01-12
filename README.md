# DNSmasq

## Usage

### Testing: 

```
docker run \
    --rm -it \
    --publish 127.0.0.1:53:53/udp \
    --volume $PWD/dnsmasq.conf:/etc/dnsmasq.conf:ro \
    --volume $PWD/dnsmasq.d:/etc/dnsmasq.d:ro \
    ghcr.io/jzizka91/docker-dnsmasq:latest
```

### Production:

```
docker run -d \
    --name dnsmasq \
    --publish 53:53/udp \
    --volume $PWD/dnsmasq.conf:/etc/dnsmasq.conf:ro \
    --volume $PWD/dnsmasq.d:/etc/dnsmasq.d:ro \
    ghcr.io/jzizka91/docker-dnsmasq:latest
```
