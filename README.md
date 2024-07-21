# Architecture Diagram
![Architecture Diagram](assets/architecture.png)

# Services
## Product Service
- Create and view products, act as a catalog
- Talks to a Mongodb instance

## Order Service
- Can order products, needs to communicate with inventory and notificaiton services, synchronously and asynchronously respectively.
- Talks to a MySQL db instance

## Inventory Service
To check whether or not a product is in stock
- Talks to a MySQL db instance

## Notification Service
- On successful order placement, send a notifcation for acknowledgement
- Stateless service, no db

