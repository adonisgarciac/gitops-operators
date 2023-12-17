# gitops-operators

## Install gitops

```
oc apply -f ocp-gitops/subscription.yaml
```

Wait until openshift-gitops is ready

## Patch openshift-gitops
Patch openshift-gitops to add resourceHealthChecks

```
oc patch ArgoCD openshift-gitops --patch-file ocp-gitops/patch.yaml -n openshift-gitops --type merge
```

## Create appset

```
oc apply -f ocp-gitops/operators-appset.yaml -n openshift-gitops
```