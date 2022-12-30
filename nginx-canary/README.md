```sh
minikube start
minikube addons enable ingress
minikube tunnel

curl -H "Host: example.com" http://127.0.0.1

for i in $(seq 1 10); do curl -s -H "Host: example.com" http://127.0.0.1 | grep -o "Version: .[0-9.]*"; done

for i in $(seq 1 10); do curl -s -H "Host: example.com" -H "x-region: eu-central-1" http://127.0.0.1 | grep -o "Version: .[0-9.]*"; done
```
