[![Dockerhub](https://img.shields.io/badge/Dockerhub-composer-blue)](https://hub.docker.com/r/ccdirk/composer)

# Composer 2.2.6

All container based on phpx.x-alpine3.x.

## simple usage

```shell
$ docker run --rm --interactive --tty \
  --volume $PWD:/app \
  ccdirk/composer:<tag> <command>
```

## using ssh-key for protected repositories

```shell
$ eval $(ssh-agent); \
 docker run --rm --interactive --tty \
   --volume $PWD:/app \
   --volume $SSH_AUTH_SOCK:/ssh-auth.sock \\
   --env SSH_AUTH_SOCK=/ssh-auth.sock \
   --volume ~/.ssh:/root/.ssh \
   ccdirk/composer:<tag> 
```