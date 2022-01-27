Service Practice (2)
================

Note that, none of Microservice A or B can be reached by external network.
When communicating between Microservices, you can't use the IP assigned by K8S.

1. ``kubectl apply -f ms_a.yaml``

2. ``kubectl apply -f ms_b.yaml``

3. ``kubectl exec -it tutum-7f8b99d4d7-2cgnp  -- wget -O- "http://ms-b:9002""``

4. ``kubectl exec -it nginx-cbbcd6f88-t9f67  -- wget -O- "http://ms-a:9001"``
