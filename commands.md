## Command
- `minikube start` - start a kubernetes cluster in development.
- `minikube stop`
- `minikube ip` - get minikube's IP address.
- `kubectl` - allows you to interact with nodes(virtual machines) in your cluster.
- `kubectl apply -f <path and filename>` - feed a config file to `kubectl`. `-f` means you want to specify a file. `apply` means we want to change the configuration of our cluster.
- `kubectl get pods` - prints the status of all running pods. `get` means we want to retrieve information about a running object.
  - `kubectl get services`
  - `kubectl get deployments`
- `kubectl describe <type> <name>` - get detailed info about an object
- `kubectl delete -f <path to config file>` - delete object.
- `kubectl set <property> <object_type> / <object_name> <container_name> = <new image to use>` - imperative command to update a property.
  - `kubectl set image <object_type> / <object_name> <container_name>  = <new image to use>` - imperative command to update an image.

---