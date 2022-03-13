# Kubeset
Installs necessary modules so that I don't have to guess what is working and what is not.

curl https://www.npmjs.com/install.sh | sudo sh
curl -LO https://storage.googleapis.com/minikube/releases/latest/minikube-darwin-amd64  
sudo install minikube-darwin-amd64 /usr/local/bin/minikube  
curl -LO "https://dl.k8s.io/release/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/darwin/amd64/kubectl"
kubectl apply -f https://k8s.io/examples/application/guestbook/redis-leader-deployment.yaml
curl -LO "https://dl.k8s.io/release/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/darwin/amd64/kubectl.sha256"
echo "$(<kubectl.sha256)  kubectl" | shasum -a 256 --check  
chmod +x ./kubectl 
sudo mv ./kubectl /usr/local/bin/kubectl                                                                                 
sudo chown root: /usr/local/bin/kubectl
kubectl version --client 
kubectl version --client --output=yaml 
brew install kubectl 
