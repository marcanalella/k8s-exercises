Service Practice
================

1. Create a deployment using nginx image

2. Create a service to expose nginx deployment

``kubectl apply -f solution.yaml``

3. Open your favourite browser and go to the cluster ip (localhost on windows, minikube ip on unix) and port to see nginx response 

if you use Docker Desktop (Windows / Mac)

``curl localhost:$NODE_PORT``


if you use Minikube on Ubuntu

``curl $MINIKUE_IP:$NODE_PORT``