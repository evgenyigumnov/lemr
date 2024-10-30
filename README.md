# lemr


```bash
helm install lemr ./lemr                                                                                                                                                                                                                                       NAME: lemr                                                                                                                                                                                                                                                                    LAST DEPLOYED: Wed Oct 30 13:32:17 2024                                                                                                                                                                                                                                       NAMESPACE: default                                                                                                                                                                                                                                                            STATUS: deployed                                                                                                                                                                                                                                                              REVISION: 1                                                                                                                                                                                                                                                                   NOTES:                                                                                                                                                                                                                                                                        1. Get the application URL by running these commands:                                                                                                                                                                                                                           export POD_NAME=$(kubectl get pods --namespace default -l "app.kubernetes.io/name=lemr,app.kubernetes.io/instance=lemr" -o jsonpath="{.items[0].metadata.name}")                                                                                                              export CONTAINER_PORT=$(kubectl get pod --namespace default $POD_NAME -o jsonpath="{.spec.containers[0].ports[0].containerPort}")                                                                                                                                             echo "Visit http://127.0.0.1:8080 to use your application"                                                                                                                                                                                                                    kubectl --namespace default port-forward $POD_NAME 8080:$CONTAINER_PORT                                                                                                                                                                                                                                                                                     
```

```bash
kubectl get pods -l app.kubernetes.io/name=lemr
```

```bash
kubectl logs -l app.kubernetes.io/name=lemr -f




EXTERNAL-IP
```bash
kubectl get svc lemr
```


PORT FORWARD

```bash
export POD_NAME=$(kubectl get pods --namespace default -l "app.kubernetes.io/name=lemr,app.kubernetes.io/instance=lemr" -o jsonpath="{.items[0].metadata.name}")  
export CONTAINER_PORT=$(kubectl get pod --namespace default $POD_NAME -o jsonpath="{.spec.containers[0].ports[0].containerPort}")
echo "Visit http://127.0.0.1:8080 to use your application"   
kubectl --namespace default port-forward $POD_NAME 8080:$CONTAINER_PORT 
```



helm uninstall lemr