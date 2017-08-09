# sonarqube-jenkins-vagrant

## Get Started

### Install vagrant-docker-compose

```
./setup
```

###  Setup sonarqube with jenkins with Vagrant

```
vagrant up
```

## How to get Jenkins' password

Login to the box

```
vagrant ssh
```

List docker containers

```
sudo docker ps
```

Find the container ID(for example `7144f7a232cf`) of image jenkins and check the logs

```
sudo docker logs 7144f7a232cf
```

The password is in the logs.
