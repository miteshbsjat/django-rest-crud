# DJANGO based REST CRUD APIs

Django based REST CRUD APIs runnable using docker.

## Build Docker Image

```bash
docker-compose build
```

## Run Django REST API listening on port `8000`

```bash
docker-compose up
```

##  Testing the API

### (CREATE) Post some records

```bash
$ curl -XPOST -H 'Content-Type:application/json' -d '{"name":"aaa","email":"aaa@mail"}' localhost:8000/users/create
{"id":2,"name":"aaa","email":"aaa@mail"}
$ curl -XPOST -H 'Content-Type:application/json' -d '{"name":"bbb","email":"bbb@mail"}' localhost:8000/users/create
{"id":2,"name":"bbb","email":"bbb@mail"}
```

### (READ) Get records
```bash
$ curl -XGET -H 'Content-Type:application/json' localhost:8000/users/
[
  {
    "id": 1,
    "name": "aaa",
    "email": "aaa@mail"
  },
  {
    "id": 2,
    "name": "bbb",
    "email": "bbb@mail"
  }
]
```
