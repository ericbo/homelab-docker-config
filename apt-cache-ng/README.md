# Apt-Cache NG

This is a simple apt cache server I use to reduce the deployment & update time of my debian
based hosts/containers. The Dockerfile was pulled right from the offical 
[Docker Docs](https://docs.docker.com/engine/examples/apt-cacher-ng/).

## Building the Image
```
docker build -t apt-cache-ng .
```

## Running the Container
```
docker run -d -p 3142:3142 -v ./local/cache:/var/cache/apt-cacher-ng --name deb-cache apt-cache-ng
```

## Pushing to a Local Registry
```
docker tag apt-cache-ng registry.domain.com/username/apt-cache-ng
docker push registry.domain.com/username/apt-cache-ng
```
