https://operatorhub.io/

https://github.com/abalki001/mariadb-operator/blob/master/Makefile

# Installer l'operator mariadb-operator, dans le namespace mariadb
cd "C:\Apps\k8s-training\k8s-mariadb-operator\mariadb-operator\helm"
helm install mariadb-operator --create-namespace -n mariadb .

# Voir les releases helm dans le namespace mariadb
helm list -n mariadb

# Montrer la CustomResource (CR) de type mariadb
kubectl get MariaDB -n mariadb

# Montrer les pods liés au setup de l'opérator
kubectl get po -n mariadb --watch

# Supprimer l'opérator
helm uninstall mariadb-operator -n mariadb


 # connect to database mariadb
 mysql -h <minikube_ip> -P 30685 -u db-user -pdb-user
 mysql -h 192.168.161.3 -P 30685 -u db-user -pdb-user

> show databases;
> use test-db;
> show tables;
