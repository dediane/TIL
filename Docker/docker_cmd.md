# DOCKER MOST USED COMMAND

## Build a container
``docker build -t -d [image name] [path to the dockerfile]``

### voir les containers actifs:
``docker ps``

### voir les tous les containers:
``docker ps -a``

### supprimer des containers:
``docker rm [container]``
#### forcer la suppression d'un container actif:
``docker rm -f [container]``

#### voir les images docker:
``docker images``

#### supprimer des images docker:
``docker rmi [nom del'image]``
#### run un container
``docker run [nom du container]``
