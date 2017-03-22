# Troubleshooting

## Debugging containers with docker exec

This can be accomplished by grabbing the container ID with a docker ps, then passing that ID into the docker exec command:

```
$ docker ps
CONTAINER ID        IMAGE
ce9de67fdcbe        apinf/platform:latest
```

```
$ docker exec -it ce9de67fdcbe /bin/bash
root@ce9de67fdcbe:/#
```

Add alias to bash:
```
alias apinf_web='docker exec -it `docker ps | grep web | sed "s/ .*//"` /bin/bash'
```