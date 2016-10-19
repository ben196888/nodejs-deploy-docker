nodejs-dev-docker
====

How to build:
```shell
docker build -t nodejs-deploy:1.2 .
```

Preparation:

You should add a shell script named `start.sh` in the root of your app folder.

How to run:
```shell
docker run -d -P --name some-nodejs-deploy-name --link --some-database:database -v /path/to/build/folder/:/opt nodejs-deploy:1.2
docker exec -it some-nodejs-deploy-name bash -l
```
