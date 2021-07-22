# Learn VueJS with Docker
```
This is a repo for learn about linking autobuild github with Docker Hub.
Check tag before pull & run.
```

# Testing
```
This image has been succsessfully created, try this:
Clone this repo
$ cd Docker-VueJS
$ npm cache clean --force
$ rm package-lock.json
$ rm -r node_modules
$ docker build -t vue1 .
$ docker run -d -p 80:80 vue1

Access on : http://localhost
```

```
This template is from VueJS "Argon" [https://vuejs.org/resources/themes.html]
```
