# Solution

0. ``kubectl create namespace test``

1. ``docker build -t app .`` and ``kubectl -n test apply -f job.yml``

2. ``kubectl describe job/app``

3. ``kubectl logs job/app``

4. ``kubectl delete job app``


