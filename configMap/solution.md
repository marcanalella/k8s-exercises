# Solution

0. ``kubectl create namespace test``

1. ``kubectl -n test apply -f configMap.yml``

2. ``kubectl -n test get configmap``

3. ``kubectl -n test describe configmap eng-config``

4. ``kubectl -n test apply -f pod.yml``

5. ``kubectl exec --stdin --tty myapp -- /bin/bash`` and inside container shell ``$ env`` ---> You will see env properties

6. ``kubectl apply -f configMap2.yml``

7. Restart pod with the two new envs ``kubectl -n test apply -f pod.yml`` 

8. ``kubectl exec --stdin --tty myapp -- /bin/bash`` and inside container shell ``$ env`` ---> You will see env properties

9. ``ls /config/`` --> You will see env properties

10. ``kubectl -n test delete namespace test``