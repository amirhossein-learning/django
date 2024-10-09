# SimpleCD

SimpleCD (aka simple continuous delivery) is a cloned application for current CD tools like ArgoCD, Jenkins, and Flux. It is being used to deploy applications on Kubernetes cluster.
It can be installed on Kubernetes clusters or any local machines. I call it SimpleCD because it's logic is so basic and simple. First you give your desired repositories as a source, then, as a destination you need to specify a Namespace. Moreover, if you want to deploy SimpleCD on a Kubernetes cluster, you have to create a serviceAccount with cluster-admin role provided. On the other hand, if you are running SimpleCD on a local machine, make sure to specify the kubernetes API server address and a authentication token with cluster-admin role.

Each instance of `simple-cd`, get the information of a git repository, and the credentials needed to communicate with a Kubernetes API. Then, it will run a git command to see if the upstream has changed or not. If so, it will pull the changes and apply them to the Kubernetes API.

## Steps

- [ ] Base git different logic
- [ ] Access to the given namespace
- [ ] Apply cloned git repository to the given namespace
- [ ] Monitor for successful apply or any failures
