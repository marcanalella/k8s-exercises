# Solution

0. ``kubectl create namespace test``

1. ``kubectl apply -f .\deployment.yml -n test``

2. ``kubectl describe deployment myapp -n test``

2. ``kubectl describe pods myapp -n test``

3. ``kubectl scale --replicas=3 -f .\deployment.yml -n test``

4. ``kubectl describe deployment myapp -n test``
`
4.  ``kubectl get pods -n test ``

5.  ``kubectl logs <pod-name> -n test`` or  ``kubectl -n test logs -f deployment/myapp``

6.  ``kubectl delete ns test ``


