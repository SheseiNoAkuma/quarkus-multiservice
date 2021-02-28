# how to use kubectl

take a look at [kubectl cheatsheet](https://kubernetes.io/docs/reference/kubectl/cheatsheet/)

## Kubectl context and configuration
* `kubectl config get-contexts`                          # display list of contexts
* `kubectl config current-context`                       # display the current-context
* `kubectl config use-context my-cluster-name`           # set the default context to my-cluster-name

## Creating objects
* `kubectl apply -f ./my-manifest.yaml`            # create resource(s)
* `kubectl apply -f ./my1.yaml -f ./my2.yaml`      # create from multiple files
* `kubectl apply -f ./dir`                         # create resource(s) in all manifest files in dir

## Deleting resources
* `kubectl delete -f ./pod.json`                                              # Delete a pod using the type and name specified in pod.json
* `kubectl delete pod,service baz foo`                                        # Delete pods and services with same names "baz" and "foo"
* `kubectl delete pods,services -l name=myLabel`                              # Delete pods and services with label name=myLabel
* `kubectl -n default delete pod,svc --all`                                      # Delete all pods and services in namespace default,

## in short
* `kubectl config use-context docker-desktop`   # set your current cluster to docker-desktop (default cluster in docker for windows)
* `kubectl apply -f .` # creates all resources described in current folder
* `kubectl delete -f .` # destroy all resources described in current folder

connect to postgres with `jdbc:postgresql://localhost:30432/postgres` admin/password
