# k8s-ingress

Pre-req*

1. Kubernetes cluster
2. Kubectl installed
3. Helm installed


1️⃣ Install NGINX Ingress Controller
--------------------------------

helm repo add ingress-nginx https://kubernetes.github.io/ingress-nginx
helm repo update

helm install nginx-ingress ingress-nginx/ingress-nginx \
  --namespace ingress-nginx --create-namespace \
  --set controller.service.type=LoadBalancer

---------------------------------

kubectl get svc -n ingress-nginx

