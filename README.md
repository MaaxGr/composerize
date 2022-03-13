# Composerize Docker

Just a docker wrapper for [magicmark/composerize](https://github.com/magicmark/composerize).

## Getting started

### Simple
```
docker run -it maaxgr/composerize:1.0.6 composerize \
    docker run -d --name web1 --net mynetwork jmalloc/echo-server:latest
```


### With function

Declare the following in `.bashrc`:
```
composerize() {
    docker run -it maaxgr/composerize:1.0.6 composerize "$@"
}
```

Run function:
```
composerize docker run -d --name web1 --net mynetwork jmalloc/echo-server:latest
```