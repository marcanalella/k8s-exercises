# Solution

0. ``kubectl create namespace test``

1. ``docker build -t app .``

2. ``kubectl -n test apply -f cronJob.yml``

3. ``kubectl get cronjob app --watch``

4. ``kubectl delete cronjob app``