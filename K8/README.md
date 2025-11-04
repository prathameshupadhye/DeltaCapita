This Project setup a new client API 

The following is the structure for the project:

1. namespace.yaml – creates namespaces for isolation  
2. deployment.yaml – deploys the Clients API  
3. service.yaml – exposes the API   
4. mongo.yaml – deploys MongoDB  
5. letsencrypt.yaml – configures Let's Encrypt  
6. certificates.yaml – requests an SSL certificate  
7. ingress.yaml – exposes API via LoadBalancer with HTTPS



Run the following command to deploy everything

```bash
kubectl apply -f K8/