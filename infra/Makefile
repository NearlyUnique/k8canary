# Infrastructure

IMAGE:=aardvark
PREFIX:=nearlyunique

list-goals: # default, list the goals for this makefile
	@ag '^[a-z-_]+' -s --nonumbers Makefile
logs:       # show the logs
	kubectl logs deployment.apps/${IMAGE}-deployment
load:
	 minikube image load ${PREFIX}/${IMAGE}
dashboard:  # show the dashboard
	minikube dashboard
list-pods:  # list available pods
	kubectl get po -A
apply:      # Apply k8s changes
	kubectl apply -f .
start-mini: # start minikube server
	minikube start
