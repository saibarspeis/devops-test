# devops-test
Use the sequence of commands:
# sudo apt install ansible
# ansible-galaxy collection install community.docker
# ansible-playbook run_docker.yaml

Once the project has been started, there will be two containers:

1. nginx-proxy container which is based on jwilder image for an nginx-proxy configured to forward all http requests to an
2. api container which exposes port 8080 to the nginx-proxy container so that http requests can be served.

The ansible playbook already runs curl http://server-api.test as a testing phase at the end and prints out the output but you can check for yourself.

This demonstrates the connectivity and transferring of the data from one container two the customer using a middleware or proxy container.

# Reasoning

The api server is built using a golang class with the golang compiler.
The most wildly used nginx proxy image is used here to demonstrate the ability to attach multiple workers to an nginx server using url hostnames rather than suffix paths

The entire stack should be executable using ubuntu distro. I am using an arm version of ubuntu so things might be slightly different.
