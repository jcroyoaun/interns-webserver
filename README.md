# Interns-webserver

This is a study case on how to approach the container creation and architecture for a FastAPI app as a DevOps engineer using an nginx reverse proxy to the Python backend and a PostgreSQL for persisting data.

This app works in conjunction with repos

* interns-db
* interns-backend-api

1. Interns DB should get started first
2. Interns Backend API should get started second
3. Lastly, we start interns Webserver


### Step #3 to run interns Webserver

1. Deploy kubernetes deployment and services
```
kubectl apply -f .
```

2. Run a port forward to expose a port on your local
```
kubectl port-forward service/nginx 8080:80
```