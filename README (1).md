This is based on the original [voting-app](https://github.com/teaguejobs/voting-app) repository from the [docker-examples](https://github.com/dockersamples) GitHub page

and modified it to work on the Kubernetes cluster.

**Commands to setup Deployments**

`kubectl create -f voting-app-deployment.yml`
`kubectl create -f voting-app-service.yml`

`kubectl create -f redis-deployment.yml`
`kubectl create -f redis-service.yml`

`kubectl create -f postgres-deployment.yml`
`kubectl create -f postgres-service.yml`

`kubectl create -f worker-app-deployment.yml`

`kubectl create -f result-app-deployment.yml`
`kubectl create -f result-app-service.yml`

**TO CHECK OUR DEPLOYMENTS**
 
`kubectl get deploy,svc`

**TO ACCESS VOTING-APP URL AND RESULT-APP URL**

`minikube service voting-service --url`
`minikube service result-service --url`

**TO SCALE OUR DEPLOYMENTS**

`kubectl scale deployment voting-app-deployment  --replicas=3`







