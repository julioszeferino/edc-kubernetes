# Apache Airflow

### Subindo o Cluster na AWS EKS
```bash
eksctl create cluster --name=clusterigtik8s --managed --instance-types=m5.large --spot --nodes-min=2 --region=us-east-2 --alb-ingress-access --node-private-networking --full-ecr-access --nodegroup-name=ng-clusterigtik8s --color=fabulous --version=1.22
```

- https://airflow.apache.org/docs/helm-chart/stable/index.html

```bash
$ kubectl create namespace airflow

# instalando o chart oficial
$ helm repo add apache-airflow https://airflow.apache.org
$ helm repo update
```

- Buscando o arquivo de values
```bash
$ cd kubernetes
$ helm show values apache-airflow/airflow  > airflow/myvalues.yaml
```
