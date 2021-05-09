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

#### run vers shell d'un container:
``docker run -ti [nom du container]``

#### delete all container:
``docker rm -f $(docker ps -a -q)``

#### delete all images:
``docker rmi -f $(docker images)``

#### run container:
``docker run -ti -p80:80 -p443:443 [NAME]``
``docker run -ti --env AUTOINDEX=on -p80:80 -p443:443 [NAME]``

### exec a container 
``docker exec -ti [NAME] bash``


