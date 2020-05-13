npx create-react-app my-react-app

cd my-react-app

docker build -t my-react-app .

docker tag my-react-app eu.gcr.io/ssil1-258911/my-react-app:tag1

docker push eu.gcr.io/ssil1-258911/my-react-app:tag1

gcloud container clusters create --machine-type n1-standard-2 --num-nodes 2  --zone europe-west2-b --cluster-version latest test-cluster

kubectl create deployment my-react-app --image=eu.gcr.io/ssil1-258911/my-react-app:tag1

kubectl expose deployment my-react-app --type LoadBalancer --port 80 --target-port 80

kubectl apply -f k8s-my-react-app.yml