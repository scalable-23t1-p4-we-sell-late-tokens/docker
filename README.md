# docker

# The repo connect to this repository:
 - Frontend: https://github.com/scalable-23t1-p4-we-sell-late-tokens/frontend
 - Order Creation Service: https://github.com/scalable-23t1-p4-we-sell-late-tokens/Create-Order-Service
 - Process Payment Service: https://github.com/scalable-23t1-p4-we-sell-late-tokens/Process-Payment-Service
 - Update Inventory Service: https://github.com/scalable-23t1-p4-we-sell-late-tokens/Update-Inventory-Service
 - Delivery Service: https://github.com/scalable-23t1-p4-we-sell-late-tokens/Deliver-Order-Service

# Instructions:
This repo fetch from ghcr.io images to deploy, so login to ghcr.io before doing anythin:
 - echo <ghcr.io_login_token> | docker login ghcr.io -u <your_username> --password-stdin
The token can be found in the canvas submission textbox

Deploying:
To deploy, starts you minikube by:
 - minikube start
Then tunnel it or port forward it, you can tunnel minikube by:
 - minikube tunnel
Then change directory to k8s/ directory and do:
 - kubectl apply -f .
Wait for a bit until all the components are up an running, then access the application through the ip address you've portforwarded or tunneled.

(In case kubectl doesn't work):
Docker compose:
Run docker compose up -d, wait for the service to starts.
Then you can access the frontend by going to:
 - localhost:5173
