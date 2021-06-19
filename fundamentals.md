## Fundamentals
- Kubernetes expects all images to already be built
- One config file per object we want to create.
- We have to manually set up networking.
- Config files are used to create objects.
- In kubernetes, objects serve different purposes - running a container, monitoring a container, setting up networking, etc.
  - Object Types:
    - Stateful Set
    - Replica Controller
    - Pod
    - Service
- The master controls your whole kubernetes cluster.
---

## Pod
- A grouping of containers with a very common purpose.
- They are inside of nodes.
- The smallest thing that we can deploy to run a single container is a pod.
- We must run one or more containers in a pod.
- Each container that is placed in a pod should have a tightly coupled relationship.
---

## Service
- Sets up networking in a kubernetes cluster.
- Subtypes of services:
  - `ClusterIP`
  - `NodePort` - Exposes a container to the outside world(only good for dev purposes)
  - `LoadBalancer`
  - `Ingress`
---

## Deployment
- Maintains a set of identical pods, ensuring that they have the correct config and that the right number exists.
- Runs a set of identical pods(one or more)
- Monitors the state of each pod, updating as necessary
- Good for development
- Good for production
- Deployment contains pod templates which is pretty much a blueprint of how every pod created by it should look.
---

## Inside A Node
- Pods and services both run inside of nodes along with kube-proxies
- `kube-proxy` - is the one single window to the outside world in a node.
- Anytime a request comes to a node it's going to flow through the kube-proxy.
- The kube-proxy will inspect the request and determine how to route it to different services.
- `label - selector` system - it allows a service to know how to set up networking for a pod by using `selector` with the pod's label.
---

## Kubernetes Important Points
- Kubernetes is a system to deploy containerized apps
- Nodes are individual machines(or vm's) that run containers
- Masters are machines(or vm's) with a set of programs to manage nodes
- Kubernetes doesn't build our images, it gets them from somewhere(Docker hub)
- Kubernetes(the master) decided where to run each container - each node can run a dissimilar set of containers
- To deploy something, we update the desired state of the master with a config file.
- The master works constantly to meet your desired state.
---