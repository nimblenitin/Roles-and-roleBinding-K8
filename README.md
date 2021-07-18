# Roles-and-roleBinding-K8
An RBAC Role contains rules that represent a set of permissions. A Role always sets permissions within a particular namespace; when you create a Role, you have to specify the namespace it belongs in.

Simple example to demonstrate Role and roleBinding based access  in Pods-

Steps followed:

*As Root*
```

1. Create the Role and roleBinding
$ vi role.yaml
$ vi roleBinding.yaml
$ kubectl apply -f role.yaml
$ kubectl apply -f roleBinding.yaml

2. Checkout the role and roleBinding created
$ Kubectl get roles
$ Kubectl get roleBinding

3. Check whether user has the access as per the roleBinding
$ kubectl auth can-i get pods --as Nitin

  ```
  *As Root*
