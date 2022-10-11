https://operatorhub.io/

https://github.com/abalki001/mariadb-operator/

# *** Deprecated since CR (Custom Resources) files below, are in same folder as mariadb-operator helm templates. ***
mariadb.persistentsys_v1alpha1_backup_cr.yaml
mariadb.persistentsys_v1alpha1_mariadb_cr.yaml
mariadb.persistentsys_v1alpha1_monitor_cr.yaml

# Installer une instance de mariadb à partir de mariadb-operator (pré-requis), dans le namespace mariadb
cd "C:\Apps\k8s-training\k8s-mariadb-operator\mariadb.old\helm"
helm install mariadb --namespace mariadb .

# Voir les releases helm dans le namespace mariadb
helm list -n mariadb

# Observer les pod dans le namespace mariadb
kubectl get po -n mariadb --watch

# Supprimer l'instance qu'on a appelé "mariadb" qui est de type mariadb:
# kubectl delete <CR_type> <releaseName>
kubectl delete mariadb mariadb
