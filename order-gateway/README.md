docker image build -t order-gateway3 .

docker run -p 8085:8085 order-gateway3
//il faut tout d'abord pusher l'image dans le repo
docker login --username username
docker tag order-gateway3 srourzaher/order-gateway3
docker push srourzaher/order-gateway3

kubectl apply -f deployment.yaml --namespace=zsr

kubectl expose deployment order-gateway3 --type=LoadBalancer --name=order-gateway-service --namespace=zsr