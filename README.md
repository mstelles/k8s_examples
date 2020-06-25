### <span style="font-family: times, serif; font-size:16pt; font-style:italic;"> Kubernetes sample manifest files

<span style="font-family: calibri, Garamond, 'Comic Sans MS' ;"> Collection of sample manifest files for multiple purposes on kubernetes.</span>

* Select the one that better suits your need and apply with <b>kubectl</b> command.
```
kubectl apply -f <file>.yaml
```
* <b>myhttpd-dev-alb.yaml:</b> creates a deployment with 2 replicas of a custom apache2 based http server container, shipped with some troubleshooting tools. Also launches an ALB (AWS) in front of the pods. </b>
* <b>efs-csi.yaml:</b> creates a PV which uses an EFS to store the files, mounting it in different sub-directories.</b>
<br>EFS must be set beforehand with the sub-directories created. Also, the worker mustc have the efs-utils package installed.
<br>To check the EFS ID:
<br>aws efs describe-file-systems --query 'FileSystems[].FileSystemId'
<br>To apply:
```
kubectl apply -f https://raw.githubusercontent.com/mstelles/k8s_examples/master/<manifest>.yaml
```
Useful commands to check:
```
kubectl get deploy
kubectl get svc -o wide
kubectl get pv
kubectl get pvc
```
