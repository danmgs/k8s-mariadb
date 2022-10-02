https://operatorhub.io/

https://github.com/abalki001/mariadb-operator/blob/master/Makefile

# Installer l'operator mariadb-operator, dans le namespace mariadb

helm upgrade --namespace mariadb --install --force mariadb-operator .

# Voir les releases helm dans le namespace mariadb
helm list -n mariadb

# Montrer la CustomResource (CR) de type mariadb
kubectl get MariaDB -n mariadb

# Montrer les pods liés au setup de l'opérator
kubectl get po -n mariadb --watch

# Supprimer l'opérator
helm uninstall mariadb-operator -n mariadb


 # connect to database mariadb
 mysql -h <ip_node> -P 30686 -u db-user -pdb-user

> show databases;
> use test-db;
> show tables;
