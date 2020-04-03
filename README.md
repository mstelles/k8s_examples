### <span style="font-family: times, serif; font-size:16pt; font-style:italic;"> Kubernetes sample manifest files

<span style="font-family: calibri, Garamond, 'Comic Sans MS' ;"> Collection of sample manifest files for multiple purposes on kubernetes.</span>

* Select the one that better suits your need and apply with <b>kubectl</b> command.
```
kubectl apply -f <file>.yaml
```
* <b>myhttpd-dev-alb.yaml:</b> creates a deployment with 2 replicas of a custom apache2 based http server container, shipped with some troubleshooting tools. Also launches an ALB (AWS) in front of the pods.
To apply:
```
kubectl apply -f https://raw.githubusercontent.com/mstelles/k8s_examples/master/myhttpd-dev-alb.yaml
```
To check:
```
kubectl get deploy
kubectl get svc -o wide
```
