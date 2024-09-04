

# python-flask-docker
Basic Python Flask app in Docker which prints the name of the worksop

### Build application
Build the Docker image manually by cloning the Git repo.
```
$ git clone https://github.com/<githubaccount>/python-flask-docker.git
$ docker build -t python-flask-docker .
```

### Download precreated image
You can also just download the existing image from [DockerHub](https://hub.docker.com/r/lvthillo/python-flask-docker/).
```
docker pull lvthillo/python-flask-docker
```

### Run the container
Create a container from the image.
```
$ docker run --name my-app -d -p 8080:8080 python-flask-docker
```

Now visit http://localhost:8080
```
 Code, Deploy, Repeat: GitHub Actions on AKS!
```

### Verify the running container
Verify by checking the container ip and hostname (ID):
```
$ docker inspect -f '{{range .NetworkSettings.Networks}}{{.IPAddress}}{{end}}' my-container
172.17.0.2
$ docker inspect -f '{{ .Config.Hostname }}' my-container
6095273a4e9b
```


