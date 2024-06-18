Running on Openshift:

Create ns infra-test-fw:

```
oc create ns infra-test-fw
```

Add necessary privileges (begin able to use root, begin able to access API resources):
```
oc adm policy add-scc-to-user privileged -n infra-test-fw -z vector
oc adm policy add-cluster-role-to-user metadata-reader -z vector -n infra-test-fw
```
