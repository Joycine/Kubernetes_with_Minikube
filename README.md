#Execute the below in minikube

eval $(minikube docker-env)
docker build -t node-app .

kubectl apply -f k8s/deployment.yaml
kubectl apply -f k8s/service.yaml




#Access the App
minikube service node-app-service
