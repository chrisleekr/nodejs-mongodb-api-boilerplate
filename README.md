# Node.js + MongoDB RESTful API Boilerplate

This is a sample project that I followed the tutorial [Build Node.js RESTful APIs in 10 Minutes](https://www.codementor.io/olatundegaruba/nodejs-restful-apis-in-10-minutes-q0sgsfhbd) written by Olatunde Garuba.

## How to start

```bash
$ docker-compose up -d
$ docker logs -f api
```

This command will build Node.js API and launch docker container [mongo](https://hub.docker.com/_/mongo/) and [mongo-express](https://hub.docker.com/_/mongo-express/)

## Endpoints

### Node.js API

| Method | URL | Sample Data |
|------- | --- | ----------- |
| GET | http://localhost:3000/tasks | |
| POST | http://localhost:3000/tasks | `{"name":"Fix issue 1"}`|
| GET | http://localhost:3000/tasks/1 | |
| PUT | http://localhost:3000/tasks/1 | `{"name":"Fix issue 1","status":"completed"}`|
| DELETE | http://localhost:3000/tasks/1 | |

### Mongo Express Dashboard

Open browser with [http://localhost:8081](http://localhost:8081)

## Troubleshooting

### Mongoose connection issue

When you download `mongo` docker image first time, then it may have a delay on initialising. As a result, `api` may throw connection exception. To resolve this issue, simply restart `api` container with below command:

```bash
$ docker-compose restart api
```
