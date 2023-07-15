This is a project on online shopping system created using Microservces Architecture in Spring Boot.

It contains of four services ->
  Product Service
  Order Serivce
  Inventory Service
  Notification Service

The product service fetches the list of products.
The order service is used to place an order and it makes a sync call to the inventory service to check which products are in stock.

I have also implemented a discovery server using Netflix Eureka.

I have implemented an API gateway using spring cloud gateway which routes the requests to either product service , order service or the discovery server.

The microservices are secured using Keycloak and Spring Security.

I have also implemeted a Circuit Breaker using Resilience4j, in case of any timeout or failure when order service calls the inventory service.

Distributed Tracing is also implemented in the project using Sleuth and Zipkin.

The order service makes an async call to the notification service using Kafka messaging queue.

Lastly, I have also tried to implement monitoring using Prometheus and Grafana(facing an issue in that, need to check).
