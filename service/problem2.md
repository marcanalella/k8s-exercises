Service Practice (2)
================

Note that, none of Microservice A or B can be reached by external network.
When communicating between Microservices, you can't use the IP assigned by K8S.

1. create a Microservice A using `karthequian/helloworld` (forget -> tutum/hello-world) image
2. create a Microservice B using `nginxdemos/hello` image
3. open a shell into Microservice A and use `wget` to reach Microservice B
4. same as 3) but in the opposite direction
