## Using maving packages
mvn package -DskipTests
mv target/spring

docker container commit {name} docker_login_name/{TAG}

## copy a file using docker
docker cp . {containder_ID}:/{location}


docker image ls
docker run -it --rm [image-id] bash/sh

docker ps is used to list images also docker images ls
docker run -idtP docker_repo_name/tag

docker build -t name/repo:v1

docker exec -it {conatiner_ID} bash

docker diff {}

docker image history docker_id/tag name


docker image push docker_repo/tag:version

docker image build -t repo_iD/tag_name:version

# Steps in creating an application

- 1. Clone the code from Github repository to local development host
- 2. Create a container based development environment build the application.
Use a pre built Maven Image which contains tooling 
- 3. Copy over the source code to this dev contianer
- 4. Connect to the container and perform all the necessary to build the application
- 5. Also do a test of the application to ensure it works fine.
- 6. Once tested, commit the container changes to an images using `docker container commit` command

docker image ls

## check failed image from the last position

docker image run -it --rm container_IDr

###
Does not fall within any known computing language

##
what is difference between docker ps and docker image ls

Build tool should not be in your final image only your runtime 

When creating an image, alway tag the repo

### Steps
- Pull a docker images
!Screenshot 2022-12-28 at 13.20.25.png
- copy the source code (src) into the docker image
docker cp . container_id or name /:{path}

final image tag should be user/repo:version

when building docker images--- docker build -f Dockerfile.ms -t (name of tag)

also/

docker build -t obasoro/new . --target=test

docker-compose mostly use for development, for production you use kubernetes

docker run -idt -p 3306:3306 \
    -e MYSQL_ALLOW_EMPTY_PASSWORD=true \
    -e MYSQL_USER_=petclinic \
    -e MYSQL_PASSWORD=petclinic \
    -e MYSQL_DATABASE=petclinic \
    mysql:5.7

docker run -idt -p 8080:8080 -e SPRING_PROFILE_ACTIVE=mysql <docker_id_name>/

docker logs <containe_id>

docker network create --driver=bridge custom

docker-compse config helps to check if 

docker-compose exec logs

dockerfile is build configuration, while docker-copose is launch configuration

Integrate Dockefile and Docker-compose

docker-compose build 
docker run -idt -p 8080:8080 \
    -e SPRING_PROFILES_ACTIVE=mysql \
    --link <cobtainer_id>:db 

