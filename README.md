# Descriptions
This app to create a PostgresSQL and Flask App

## Getting Started

1. Config k8s
kubectl apply -f configmap.yaml
kubectl apply -f pvc.yaml
kubectl apply -f pvc.yaml
kubectl apply -f pv.yaml
kubectl apply -f postgresql-deployment.yaml
kubectl apply -f coworking.yaml

2. Forward port for DB
kubectl port-forward svc/postgresql-service 5433:5432 &

3. Import data
Run ./db/*.sql

4. Serve app
    
    curl http://a0bf3d56db54e49808290d2745a9ee2e-85792453.us-east-1.elb.amazonaws.com:5153/api/reports/daily_usage

    curl http://a0bf3d56db54e49808290d2745a9ee2e-85792453.us-east-1.elb.amazonaws.com:5153/api/reports/user_visits

#Test commit