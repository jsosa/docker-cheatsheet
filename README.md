# docker-cheatsheet
Simple docker cheat sheet

#### Build docker
`docker build -t dkr-package .`

#### Run docker
`docker run -it --rm dkr-package`

#### List all images
`docker image ls`

#### Remove one or more Docker images
`docker image rm dkr-package`

#### Removing all unused objects
`docker system prune`

#### Removing all unused volumes
`docker system prune --volumes`

#### List of all active and inactive containers 
`docker container ls -a`
