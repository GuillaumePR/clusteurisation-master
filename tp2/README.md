1. Quel est le nom du contexte courant (context) ? minikube
2. Combien de nœuds voyez-vous ? 1 seul noeud

1. Quelle image exacte est utilisée ? nginx 1.27

2. Quel évènement (Events) confirme le téléchargement et le démarrage ?
  Normal  Pulling    3m19s  kubelet            Pulling image "nginx:1.27"
  Normal  Pulled     2m44s  kubelet            Successfully pulled image "nginx:1.27" in 34.897s (34.897s including waiting). Image size: 192461947 bytes.

1. À quoi sert un Service dans Kubernetes ?
le service fournit une abstraction réseau pour accéder aux pods via IP et DNS fixe
2. Pourquoi le Service n’expose-t-il pas automatiquement une IP publique en local ?
car minikube fonctionne en environnement local donc pas de cloud provider et type clusterIP est uniquement accessible à l’intérieurr

1. Que se passe-t-il au niveau des pods lors d’un changement d’image ?
kube crée un nouveau pod avec la nouvelle image et arrete l’ancien pod
2. Qu’est-ce qu’un “rollout” et pourquoi est-ce utile ?
éviter d'avoir des interruptions de service


Compte-rendu :
installé kubectl et minikube puis démarré avec minikube start --driver=docker
vérification du bon fonctionnement avec kubectl get nodes, kubectl get pods et kubectl get svc

création d'un namespace tp-minikube puis ait déployé un conteneur nginx via un deployment.yaml
le service a été exposé avec un service de type clusterIP accessible avec minikube service  --url
kubectl logs et kubectl describe pour observer l'appli

Difficultés rencontrées :
trouver ce qu'il fallait mettre précisément dans le deployment.yaml
et dans la même veine, ce qu'il fallait mettre précisément dans le service.yaml
