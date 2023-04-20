# ArgoCD
Argo CD is a declarative, GitOps continuous delivery tool for Kubernetes.

for this Project we use local minikube cluster & also you need to download Argo CD localy . 
# install ArgoCD in k8s 
kubectl create namespace argocd <br>
kubectl apply -n argocd -f https://raw.githubusercontent.com/argoproj/argo-cd/stable/manifests/install.yaml

# access ArgoCD UI
kubectl get svc -n argocd
kubectl port-forward svc/argocd-server 8080:443 -n argocd

# login with admin user and below token (as in documentation):
kubectl -n argocd get secret argocd-initial-admin-secret -o jsonpath="{.data.password}" | base64 --decode && echo


