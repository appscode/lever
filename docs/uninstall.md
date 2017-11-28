---
title: Uninstall Swift
description: Swift Uninstall
menu:
  product_swift_0.5.1:
    identifier: uninstall
    name: Uninstall
    parent: getting-started
    weight: 40
product_name: swift
left_menu: product_swift_0.5.1
section_menu_id: getting-started
url: /products/swift/0.5.1/getting-started/uninstall/
aliases:
  -- /products/swift/0.5.1/uninstall/
---

# Uninstall Swift
Please follow the steps below to uninstall Swift:

1. Delete the various objects created for Swift operator.
```console
$ ./hack/deploy/uninstall.sh
+ kubectl delete deployment -l app=swift -n kube-system
deployment "swift" deleted
+ kubectl delete service -l app=swift -n kube-system
service "swift" deleted
+ kubectl delete serviceaccount -l app=swift -n kube-system
No resources found
+ kubectl delete clusterrolebindings -l app=swift -n kube-system
No resources found
+ kubectl delete clusterrole -l app=swift -n kube-system
No resources found
```

2. Now, wait several seconds for Swift to stop running. To confirm that Swift operator pod(s) have stopped running, run:
```console
$ kubectl get pods --all-namespaces -l app=swift
```
