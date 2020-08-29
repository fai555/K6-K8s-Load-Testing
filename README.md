# Load Testing with K6 on Kubernetes

You can use these YAML manifest files to Load Test with K6 and the K6 script is deployed on top of Kubernetes.


## Installation

- Clone this repository
```
git clone https://github.com/fai555/K6-K8s-Load-Testing.git
```

- Update the `ConfigMap` named `k6-script` in the `job.yaml` file with your own load testing script.

- Deploy the yaml files to your Kubernetes cluster and the load testing script will run as a Kubernetes Job.
```
cd K6-K8s-Load-Testing

kubectl apply -f .
```

## View Grafana Dashboards
Now you can port forward into your Grafana dashboard to see the default metrics in nice dashboard that K6 gives you out of the box.
```
kubectl port-forward deployment/grafana 3000:3000
```
