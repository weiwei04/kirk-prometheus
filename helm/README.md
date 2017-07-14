### How to deploy kirk prometheus

#### Prerequest install prometheus-operator

helm repo add opsgoodness http://charts.opsgoodness.com
helm repo add cloudposse https://charts.cloudposse.com/incubator

helm install opsgoodness/prometheus-operator --name sys --namespace kube-system

#### Install kirk prometheus

1. cp values-tpl.yaml values.yaml and fill in the param

2. helm install kirk-prometheus --name kirk-monitor --namespace kube-system --values values.yaml