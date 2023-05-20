# notes

installed
* `kubectl`
* `docker`
* `minikube`

for minikube
* `minikube addons enable ingress`

# issues

## enable ingress addon

`minikube addons enable ingress` timed out every time, the logs hinted to `registry.k8s.io/ingress-nginx/controller:v1.7.0`.

Attempting to use `minikube ssh` then `docker pull` still timed out

Fix was to run. The docker pull may not be required.

```bash
docker pull registry.k8s.io/ingress-nginx/controller:v1.7.0
minikube image load registry.k8s.io/ingress-nginx/controller:v1.7.0
```
