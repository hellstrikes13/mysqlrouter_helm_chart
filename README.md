# Helm handy comands
### Author: Sudi
This is Helm chart for mysqlrouter<br>
docker image: [https://hub.docker.com/r/mysql/mysql-router/]<br>

>package the helm chart for mysqlrouter
- helm package MySQLRouter
>install the helm chart
- helm install  --name mysqlrouter MySQLRouter.tar.gz
> list the helm chart currently availabel on your k8 system
- helm list
> delete the helm permanently
- helm delete --purge mysqlrouter

##### NOTE: you need to give based64 value for this 4 variables defined under secret.yaml
to obtain base64 values
echo -n "myvalue" | base64
-  MYSQL_HOST: somevalue_base64==
-  MYSQL_PORT: somevalue_base64==
-  MYSQL_USER: somevalue_base64==
-  MYSQL_PASSWORD: somevalue_base64==
-  MYSQL_INNODB_CLUSTER_MEMBERS: >somevalue_base64==>
#### please note: network mode is set to HOST ; you might have to EDIT the source before creating package.
