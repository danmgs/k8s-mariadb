https://operatorhub.io/

https://github.com/abalki001/mariadb-operator/

# Installer une instance de mariadb à partir de mariadb-operator (pré-requis), dans le namespace mariadb
helm upgrade --namespace mariadb --install --force mariadb .

# Voir les releases helm dans le namespace mariadb
helm list -n mariadb

# Observer les pod dans le namespace mariadb
kubectl get po -n mariadb --watch

# Supprimer l'instance qu'on a appelé "mariadb" qui est de type mariadb:
# kubectl delete <CR_type> <releaseName>
kubectl delete mariadb mariadb
