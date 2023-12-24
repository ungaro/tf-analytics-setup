# tf-analytics-setup

minikube start --memory 65536 --cpus 8

```cd terraform
terraform init
terraform apply --auto-approve
kubectl port-forward svc/argocd-server -n argocd 8080:80
kubectl get secrets argocd-initial-admin-secret -o yaml -n argocd
echo "data.password" | openssl base64 -d
```