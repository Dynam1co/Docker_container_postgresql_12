# Docker_container_postgresql_12
Docker container with Ubuntu 20.04 and Postgre SQL 12

## Instructions to create image and run
Go to Dockerfile path and run (First time)
```
$ docker build -t postgresql_12_3 .
```

To create container (First time)
```
$ docker run -i -p 5432:5432 --name my_container postgresql_12_3
```

Start container (Rest of the time)
```
$ docker start my_container
```

Enter in bash:
```
$ docker run --rm -t -i --link my_container:pg postgresql_12_3 bash
```
