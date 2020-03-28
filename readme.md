# How to run it

- we create clusterIP only if there's another object (pod, service, ..etc) need to access the current object that wrapped by the clusterIP but in case no need for that we will not create clusterIP like the worker deployment it's not accessable from anywhere it just need to access other clusters so no need for clusterIP for it and no need for expose port for it 
- We need PVC --> Persistent Volume Claim
- get information about k8s storage
- `kubectl get storageclass`
- `kubectl describe storageclass`
- we can't put the password inside k8s direct as a plain text we need to store it in a secure place `Secret Object` by run the following command: `kubectl create secret generic <secret_name> --form-literal key=value`
- get all secrects `kubectl get secrets`
- minikube dashboard


kubectl create secret generic pgpassword --from-literal PGPASSWORD=admin123