Now that we have established that kubectl is running and all the components are functional, let us try to play with it a bit.

Lets create a namespace.

`kubectl create namespace dev`{{execute}}

Lets now create a pod to run nginx within the namespace.

`kubectl run nginx --image=nginx -n dev`{{execute}}

You can verify that the pod is running and inspect its IP address.

`kubectl get pods -o wide -n dev`{{execute}}

Lets now get rid of this namespace and everything within it.

`kubectl delete namespace dev`{{execute}}

You can verify that everything within `dev` is deleted using this.

`kubectl get all --all-namespaces`{{execute}}