# tf-analytics-setup

 minikube start --memory 64189 --cpus 8 --disk-size=200g

```cd terraform
terraform init
terraform apply --auto-approve
kubectl port-forward svc/argocd-server -n argocd 8080:80
kubectl get secrets argocd-initial-admin-secret -o yaml -n argocd
echo "data.password" | openssl base64 -d
```


argocd login localhost:8080 --username=admin --password="password" --insecure
