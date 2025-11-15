# argocd-quickstart

## primeiros passos

    instalar docker desktop https://docs.docker.com/desktop/setup/install/windows-install/

    habilite o wsl se pedir

    habilite o kubernetes

## argocd

    ref.: https://argo-cd.readthedocs.io/en/stable/getting_started/
    
    baixar o manifesto do argocd:
    
    wget -o argocd.yaml https://raw.githubusercontent.com/argoproj/argo-cd/stable/manifests/install.yaml

    adicionar ao service argocd-server o valor type: LoadBalancer no argocd.yaml

    kubectl create namespace argocd

    kubectl -n argocd apply -f argocd.yaml

    kubectl -n argocd apply -f argocd-app.yaml

    pegar senha admin na secret argocd-initial-admin-secret gerada automaticamente para acessar a interface em http://localhost
