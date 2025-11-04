This Project setup a new client API 

The following is the structure for project
1.namespace.yaml  for creating namespaces for isolation 
2.deployment.yaml to deploy the Client API
3.service.yaml to exposes the API
4.mongo.yaml  deploys MongoDB 
5.letsencrypt.yaml  configures Let's Encrypt
6.certificate.yaml requests an SSL certificate
7.ingress.yaml exposes API via LoadBalancer with HTTPS 



# Apply manifests in order
kubectl apply -f k8s/namespace.yaml
kubectl apply -f k8s/deployment.yaml
kubectl apply -f k8s/service.yaml
kubectl apply -f k8s/mongo.yaml
kubectl apply -f k8s/issuer.yaml
kubectl apply -f k8s/certificate.yaml
kubectl apply -f k8s/ingress.yaml
