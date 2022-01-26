Service Practice (2)
================

Note that, none of Microservice A or B can be reached by external network.
When communicating between Microservices, you can't use the IP assigned by K8S.

1. Create a Microservice A using `karthequian/helloworld` (forget -> tutum/hello-world) image ``kubectl apply -f ms_a.yaml``

2. Create a Microservice B using `nginxdemos/hello` image ``kubectl apply -f ms_b.yaml``

3. Open a shell into Microservice A and use `wget` to reach Microservice B. Here is a one-line command to achieve the goal: ``kubectl exec -it tutum-7f8b99d4d7-2cgnp  -- wget -O- "http://ms-b:9002""``

4. Same as 3) but in the opposite direction ``kubectl exec -it nginx-cbbcd6f88-t9f67  -- wget -O- "http://ms-a:9001"``