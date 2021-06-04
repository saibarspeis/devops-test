# devops-test
Use docker-compose up -d in the directory of the docker-compose.yaml file to build and run the project.

Once the project has been started, there will be two containers as fallowing:

1. nginx-proxy container which is based on jwilder image for an nginx-proxy configured to forward all http requests to an
2. api container which exposes port 8080 to the nginx-proxy container so that http requests can be served.

A simple curl http://localhost (or http://server-api.test as long as you've defined this hostname in dns or /etc/hosts) will return a json response from the api server.

This demonstrates the connectivity and transferring of the data from one container two the customer using a middleware or proxy container.
