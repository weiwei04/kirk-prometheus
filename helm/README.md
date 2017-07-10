### How to deploy kirk prometheus

#### Prerequest install prometheus-operator

helm install opsgoodness/prometheus --name sys --namespace kube-system

#### Install kirk prometheus

1. cp values-tpl.yaml values.yaml and fill in the param

2. helm install kirk-prometheus --name kirk-monitor --namespace kube-system --values values.yaml