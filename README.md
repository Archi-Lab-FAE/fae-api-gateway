# fae-api-gateway

API gateway for communication between the microservices and the user
THis project depends on the spring-cloud gateway.

## Usage

The project could be started in three different environments:

1. local
2. development
3. production

### LOCAL

For local development you can just run the project within your IDE.
The default and local configuration will be used. Register a service can be done via the local configuration file.
The server will be available on "http:localhost:8080"

### DEV

For development of other service you can run this project in development mode. There two scripts will help you start
and stop the service in docker. These script pull the image from our docker registry and start the container.
make sure your service is in the "fae_backend" network.
The service will start with the dev configuration and will be available on "http:localhost:8080".

### PROD

In our production env. YOu just have to connect your service to the service discovery.
The production mode will start two containers to ensure one is always up.
To register any route please edit the prod configuration.
