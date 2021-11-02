# What is this?

A super basic setup of hosting an express application using kubernetes that is pointing to a local docker registry hosted on port 5000.  I have no clue what I'm doing, but this works!

```
./kind-with-registry.sh
```


*Useful commands I'll probably forget if I don't write them down* 

```
kubectl get pods
kubectl get services
kubectl port-forward <POD_NAME> 7000:8000
kind delete cluster
kind delete pod <POD_NAME>
kubectl apply -f ./kubernetes
docker logs -f kind-registry
docker build -t localhost:5000/express:latest .
git push localhost:5000/express:latest
```