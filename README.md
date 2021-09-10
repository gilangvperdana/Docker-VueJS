# Learn Deploy VueJS with Docker
```
a little exploration of the deloy vue project process.
```

# Change the Project
```
If you want to change the your Vue project, just delete all file on this folder except 'Dockerfile'
```

# Testing Deploy
```
This image has been succsessfully created, try this:
Clone this repo
$ cd Docker-VueJS-Certbot
$ npm cache clean --force
$ rm package-lock.json
$ rm -r node_modules
$ docker build -t vue1 .
$ docker run -d -p 80:80 vue1

Access on : http://localhost

If you want to deploy with SSL:
Clone this repo
$ cd Docker-VueJS-Certbot
Change the Dockerfile "nginx productionstage" replace Dockerfile with sslDockerfile
$ docker build -t vuessl .
$ docker run -d -p 80:80 -p 443:443 vuessl
$ docker ps (see the container id for vuessl)
$ docker exec -it container_id_vuessl bash
$ certbot --nginx -d domain.com -d www.domain.com

Access on : https://localhost
```

```
This template is from VueJS "Argon" [https://vuejs.org/resources/themes.html]
```
