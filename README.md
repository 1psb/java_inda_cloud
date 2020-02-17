# java_inda_cloud
Project to show transition from Monolith application to clustered microservice app

# Getting started

`git checkout monolith` to start.

## Monolith

`git checkout monolith` to return.

## Standalone

`git checkout standalone` to return.

## Microservices

`git checkout microservices` to return.

## Cloud orchestration

### Theory

Containers engines provide an ability to cut the corners of `VM` style solutions and instead of heavy Guest OS you
use layered containers.

### Build

```bash
mvn clean package
```

### Deploy

```bash
docker-compose up -d --build --force-recreate

```

### Use

```bash
curl --request POST \
  --url http://localhost:8081/catalog \
  --header 'content-type: application/json' \
  --data '{
	"name": "Internet",
	"price": 500
}'
```

```bash
curl --request GET \
  --url http://localhost:8081/catalog/{specification_id}
```

```bash
curl --request PUT \
  --url http://localhost:8082/catalog/{specification_id}/order
```

### Drawbacks

- -Big codebase-
- -Risk: trespassing between modules-
- -Risk: problems with maintenance and evolution- ?
- -IDE load- ?
- -Web Container load-
- -Problems with Continuous Deployment- 
- -Limitations of environment scalability-
- -Problems with development scalability- 
- -Fixed technical stack-
- -Infrastructure dependencies- 
- Hard to test
- -Hard to configure deployment- 
- Resources consumption

