
# https://www.cncf.io/wp-content/uploads/2020/04/2020_04_Introduction-to-Kubernetes-RBAC.pdf


kubernetes-daemonsets

https://medium.com/kubernetes-tutorials/a-guide-to-kubernetes-daemonsets-6db7920ad140
https://bass.netcracker.com/pages/viewpage.action?spaceKey=AVP&title=7.0+Release+Plan

Network policy - pods commnuncations


kubernetes-security-psp-network-policy
https://sysdig.com/blog/kubernetes-security-psp-network-policy/

RBAC
https://kubernetes.io/docs/reference/access-authn-authz/rbac/

''''
apiVersion: rbac.authorization.k8s.io/v1
kind: Role
metadata:
  namespace: default
  name: pod-reader
rules:
- apiGroups: [""] # "" indicates the core API group
  resources: ["pods"]
  verbs: ["get", "watch", "list"]
  
''''

TLS CSR 

https://thenewstack.io/a-practical-approach-to-understanding-kubernetes-authentication/

https://github.com/JulienBalestra/kube-csr
