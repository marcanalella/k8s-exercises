Secrets practice
==================

# Image requirements
------------------

The image 'postgres' requires one env var:
- POSTGRES_PASSWORD

# Practice
------------------

1) Create a secret named 'eng-secret' with kubectl and a yaml file to define the password. Password value must be the output of

``echo -n 'password' | base64 ``

2) Verify that has been created using kubectl
3) Describe the secret with kubectl. You should not see the clear password.
4) Use the secret in a pod using the 'postgres' image
5) Verify the pod is using the correct env by executing the 'env' command in the running pod. You should see POSTGRES_PASSWORD=clear-pass
6) Clean up
