This Project setup a new client API 

The following is the structure for the project:

1. namespace.yaml – creates namespaces for isolation  
2. deployment.yaml – deploys the Clients API  
3. service.yaml – exposes the API internally  
4. mongo.yaml – deploys MongoDB  
5. letsencrypt.yaml – configures Let's Encrypt  
6. certificates.yaml – requests an SSL certificate  
7. ingress.yaml – exposes API via LoadBalancer with HTTPS



Run the following commands **in order** to deploy everything:

```bash
kubectl apply -f k8s/namespace.yaml
kubectl apply -f k8s/deployment.yaml
kubectl apply -f k8s/service.yaml
kubectl apply -f k8s/mongo.yaml
kubectl apply -f k8s/letsencrypt.yaml
kubectl apply -f k8s/certificates.yaml
kubectl apply -f k8s/ingress.yaml