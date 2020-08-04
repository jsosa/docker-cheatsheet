# docker-cheatsheet
Simple docker cheat sheet

#### Build docker
`-t` tagname
```
docker build -t dkr-package .
```

#### Autheticate in Docker Hub
```
docker login
```
#### Commit an image
`message` commit message

`NAME` fullname

`USER` Docker Hub username
```
docker commit -m "message" -a "NAME" test-lamp-server USER/dkr-package:latest
````

#### Push image to registry
`USER` Docker Hub username
```
docker push USER/dkr-package
```

#### Run docker
`-it` interactive processes (like a shell)

`--rm` will remove a container upon exit, not the image!
```
docker run -it --rm dkr-package
```

#### Call an application from a docker
`--rm` will remove a container upon exit, not the image!

`app-path` application living in the container
```
docker run --rm dkr-package app-path
```

#### Mount a volume on a container and run an application
`path1` is the absolute path to the folder to mount in the container

`path2` is the path in the cotainer where to locate that folder

`app-path` application living in the container
```
docker run -v <path1>:<path2> dkr-package app-path
```

#### List all images
```
docker image ls
```

#### Remove one or more Docker images
```
docker image rm dkr-package
```

#### Removing all unused objects
```
docker system prune
```

#### Removing all unused volumes
```
docker system prune --volumes
```

#### List of all active and inactive containers 
```
docker container ls -a
```
