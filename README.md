# Docker installation and how to start using it

## Install Docker on Ec2 instance

```
sudo apt install docker.io -y
```

### Start Docker Daemon

```
sudo systemctl start docker
```

### Check the status of Docker Daemon

```
sudo systemctl status docker
```

### Provide access to run docker commands

> If your user name is different from ```ubuntu``` you can change the username as per the requirement

```
sudo usermod -aG docker ubuntu
```

> Note : You need to logout and login back for the changes to be reflected

### Verify docker is installed and in active state

```
docker run hello-world
```

## Login to Docker

> Create a account if not present on ```https://hub.docker.com/```

```
docker login
```

> Provide username and password same which you used to login on dockerhub

### Build Docker Image

> Change username ```azharmir``` to username using which you login to dockerhub

```
docker build -t azharmir/simple-hello-world:latest .
```

> Note: "-t" is used to apply a docker image tag to a build

### Check Docker Image

```
docker images
```

### Run Docker Container

```
docker run -it azharmir/simple-hello-world
```

> Note: "-it" is short for ```interactive```. When you use docker run with this command it takes you straight inside the container

### Push the Image to DockerHub

```
docker push azharmir/simple-hello-world
```

> Login to ```https://hub.docker.com/``` to view your image on dockerhub repositories