# Docker

#### PostgreSQL 9.3
https://hub.docker.com/r/sergiorobsantos/postgresql/

docker pull sergiorobsantos/postgresql:v1

```sh
sudo docker build -t [your_user_on_docker_hub]/postgresql:[v1] [.]
```

```sh
sudo docker push image:version_tag
```

```sh
sudo docker run -d --name postgresql -p 55432:5432 sergiorobsantos/postgresql:v1
```

```sh
sudo docker stats postgresql
```

```sh
sudo docker port postgresql
```
Connect to docker postgresql (user: docker, password: docker)
```sh
psql -h localhost -p 55432 -d docker -U docker --password

docker=# select datname from pg_database;
docker=# create database unisal;
```
#### Application
docker pull sergiorobsantos/my_tomca-:v2

To run tomcat detach
```sh
sudo docker run -d --name tomcat -p 10080:8080 sergiorobsantos/my-tomcat:v2
```

To see the generated admin password
```sh
sudo docker logs tomcat
```
#### Run docker.yaml
```sh
sudo docker-compose --file docker.yaml up -d
```

```sh
sudo docker-compose --file docker.yaml ps
```

```sh
sudo docker-compose --file docker.yaml down
```
