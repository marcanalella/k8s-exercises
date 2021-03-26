ConfigMap practice
==================

# Image requirements
------------------

The image 'nginx' used in the pod that you'll create in step 4), requires four env vars:
1) BASE_URL
2) MYSQL_HOST
3) MYSQL_USER
4) MYSQL_PASSWORD

# Practice
------------------

1) Create a configmap named 'eng-config' with kubectl and a yaml file. It must contain MYSQL_HOST
2) Verify that has been created using kubectl
3) Describe the configmap with kubectl
4) Use the configmap in a pod
5) Verify the pod is using the correct env by executing the 'env' command in the running pod. You should see BASE_URL and MYSQL_HOST
6) Create a new configmap containing MYSQL_USER and MYSQL_PASSWORD
7) Add these two new env vars in the pod definition using envFrom
8) Repeat 5. to see new env vars
9) Mount the configmap in the container and run a command in the pod to output the content of the mount path
10) Clean up