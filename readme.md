### Docker
    You can pull a pre-built docker image of the swagger-ui directly from Docker Hub:

## Install
    `docker pull swaggerapi/swagger-ui`
    `docker run -p 80:8080 swaggerapi/swagger-ui`
    Will start nginx with Swagger UI on port 80.

    Or you can provide your own swagger.json on your host

    docker run -p 80:8080 -e SWAGGER_JSON=/foo/swagger.json -v /bar:/foo swaggerapi/swagger-ui
    You can also provide a URL to a swagger.json on an external host:

    docker run -p 80:8080 -e SWAGGER_JSON_URL=https://petstore3.swagger.io/api/v3/openapi.json swaggerapi/swagger-ui
    The base URL of the web application can be changed by specifying the BASE_URL environment variable:

    docker run -p 80:8080 -e BASE_URL=/swagger -e SWAGGER_JSON=/foo/swagger.json -v /bar:/foo swaggerapi/swagger-ui


## Editor

    docker pull swaggerapi/swagger-editor
    docker run -d -p 80:8080 swaggerapi/swagger-editor

    docker run -d -p 80:8080 -v $(pwd):/tmp -e SWAGGER_JSON=openapi.json swaggerapi/swagger-editor