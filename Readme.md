# Install the operator first
- kubectl create namespace observability
- kubectl create -f https://github.com/jaegertracing/jaeger-operator/releases/download/v1.29.1/jaeger-operator.yaml -n observability


# Create Hotrod namespace
kubectl create namespace hotrod

# Apply the manifests
- kubectl apply -f simple.yaml
- Ensure all the pods are up and running (``kubectl get all -n hotrod``)
- kubectl apply -f hotrod/manifest.yaml



