# Solution

0. ``kubectl create namespace test``

1. ``echo -n 'password' | base64`` --> this will show you encrypted base64 password to put inside secrets.yml

2. ``kubectl -n test apply -f .\secrets.yml``

3. ``kubectl -n test get secrets eng-secret -L=POSTGRES_PASSWORD`` --> You won't see the value of password

4. ``kubectl -n test describe secrets eng-secret -o yaml`` --> Same here, you won't see the value of password

5. ``kubectl -n test apply -f .\pod.yml``

6. ``kubectl -n test exec --stdin --tty myapp -- /bin/bash`` --> inside container shell put ``$ env`` 

7. ``kubectl delete namespace test``