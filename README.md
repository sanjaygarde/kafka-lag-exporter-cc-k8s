# kafka-lag-exporter-cc-k8s
This app/tool can be used to deploy the kafka-lag-exporter (https://github.com/seglo/kafka-lag-exporter) for Confluent Cloud as a kubernetes service without use of helm charts.

Here's how you use it. First edit the klg-deployment.yaml file with details of your confluent cloud account, then you run it as below:

_kubectl apply -f klg-configmap.yaml
kubectl apply -f klg-deployment.yaml
kubectl apply -f klg-service.yaml
_
Test it as below:

Get the pod name by running:

_kubectl get pods_

And then

_./port-forward.sh <your pod name>_
