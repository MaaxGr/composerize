# Composerize Docker

Just a docker wrapper for [composerize/composerize](https://github.com/composerize/composerize).

## Getting started

### Simple
```
docker run -it maaxgr/composerize:latest composerize \
    docker run -d --name web1 --net mynetwork jmalloc/echo-server:latest
```

### Simple with existing `docker-compose.yml` file
```
docker run -it maaxgr/composerize:latest composerize \
    docker run -d --name web1 --net mynetwork jmalloc/echo-server:latest \
	< docker-compose.yml
```


### With function

Declare the following in `.bashrc`:
```
composerize() {
    docker run -it maaxgr/composerize:latest composerize "$@"
}
```

Run function:
```
composerize docker run -d --name web1 --net mynetwork jmalloc/echo-server:latest
```

Or run function with existing `docker-compose.yml` file:
```
composerize docker run -d --name web1 --net mynetwork jmalloc/echo-server:latest < docker-compose.yml
```