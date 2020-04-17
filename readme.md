# hok-operator

### Installation

Apply the CRD
```sh
$ cd deploy
$ kubectl apply -f crd.yaml
```

Create the ClusterRole, ClusterRoleBinding and ServiceAccount
```sh
$ kubectl apply -f service_account.yaml -n <NAMESPACE>
$ kubectl apply -f clusterrole.yaml
```
Edit cluster_role_binding.yaml file and add your service account namespace.  
Then apply the cluster role binding.
```sh
$ kubectl apply -f cluster_role_binding.yaml
```

Deploy the Operator
```sh
$ kubectl apply -f operator.yaml -n <NAMESPACE>
```


Deploy the CustomResource -> HokStack
Make sure to edit the required values.
```sh
$ kubectl apply -f cr.yaml -n <NAMESPACE>
```
