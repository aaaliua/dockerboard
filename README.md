
# Dockerboard

**Work-In-Process**

Simple dashboards, visualizations, managements for your dockers.

Lovingly created and maintained by [DockerPool][] Team.


## Quick Start

```
git clone github.com/dockerboard/dockerboard
cd dockerboard
cd client/
npm install
bower install

docker build -t dockerboard .
docker run -d -p 8001:8001 -v /var/run/docker.sock:/var/run/docker.sock dockerboard
open http://127.0.0.1:8001
```

### Connect vai a http/https Or a unix sock

  If using [boot2docker][], these are some ENV variables.

```
export DOCKER_HOST="tcp/0.0.0.0:2376"
export DOCKER_CERT_PATH="$HOME/.boot2docker/certs/boot2docker-vm"
export DOCKER_TLS_VERIFY="1"
```


## Screenshots

### Demo

![Dockerboard Screenshot](https://github.com/dockerboard/dockerboard/blob/master/screenshots/2-demo.gif?raw=true)

## Development

Currently it's very simple.   


### Install npm & bower packages

```
cd client/
npm install
bower install

cd ../
go get ./..
go run dockerboard.go
```


## Build With

- [gohttp](https://github.com/gohttp) &mdash; Our back end API is gohttp app. It responds to requests RESTfully in JSON.
- [Angular.js](https://www.angularjs.org/) &mdash; Our front end is an Angular.js app that communicates with the negroni API.
- [Famous.js](http://famo.us/) &mdash;  We use Famous.js to build beautiful experiences on any device.
- [D3.js](http://d3js.org/) &mdash; We use D3.js for drawing, bring data.


[DockerPool]: http://dockerpool.com/
[boot2docker]: http://boot2docker.io/
