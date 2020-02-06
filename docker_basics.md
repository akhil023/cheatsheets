clean up any resources — images, containers, volumes, and networks — that are dangling (not associated with a container):

`docker system prune`

remove any stopped containers and all unused images (not just dangling images), add the -a flag to the command:

`docker system prune -a`



sudo docker build -t <docker_image_name> -f <path_to_dockerfile> .

sudo docker images

sudo find / -iname docker

sudo docker run -p 8765:8000  --env="NODE_ENV=dev2"  test

vim Dockerfile

cat Dockerfile

sudo docker ps -a

sudo service docker status

sudo service docker start

sudo service docker stop

sudo docker ps -a -q

sudo docker rm -f $(sudo docker ps -a -q)

sudo docker rmi $(sudo docker images -a -q)

bash into it => docker exec -it 7efccd6b1738 bash

sudo docker stop 46fa4219d132
