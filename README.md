# Spring Boot Microservices

In the default configuration you will have:

- **Discovery Service** running on port `8761`, access `http://localhost:8761` to see the dashboard
- **API Gateway** running on port `8765`, you will send the requests to this service
- **Two Article Services** running on ports: `8080` and `9080`
- **Two Author Services** running on ports: `8081` and `9081`

After running the containers, head to `http://localhost:8761` to make sure that the four services (two **article** and two **author**) are registered in the **Discovery Service**, when they're all registered you can test the application with `curl` making requests to the endpoints below:

- `curl http://localhost:8765/api/articles`
- `curl http://localhost:8765/api/articles/id`
- `curl http://localhost:8765/api/articles/author/id`
- `curl http://localhost:8765/api/authors`
- `curl http://localhost:8765/api/authors/id`
