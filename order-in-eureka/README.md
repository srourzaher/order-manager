docker image build -t order-eureka .

docker run -p 8761:8761 order-eureka
//il faut tout d'abord pusher l'image dans le repo
docker login --username username
docker tag order-eureka srourzaher/order-eureka
docker push srourzaher/order-eureka

kubectl apply -f deployment.yaml --namespace=zsr

kubectl expose deployment order-eureka --type=LoadBalancer --name=order-eureka-service --namespace=zsr