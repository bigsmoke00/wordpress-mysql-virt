### 1. Criar namespace

```bash
kubectl create namespace virtualizacao &>/dev/null
```

### 2. instalar Mysql

```bash
helm install mysql -f wordpress/values-mysql.yaml bitnami/mysql --version '9.15.0' --namespace virtualizacao &> mysql.log
```

### 3. Instalar Wordpress

```bash
helm install wordpress -f wordpress/values-wordpress.yaml bitnami/wordpress --version '19.0.4' --namespace virtualizacao &> wordpress.log
```
