# gitops-operators

## Install gitops

```
oc apply -f ocp-gitops/subscription.yaml
```

Wait until openshift-gitops is ready

## Patch openshift-gitops
Patch openshift-gitops to add resourceHealthChecks

```
oc apply -f ocp-gitops/patch.yaml
```

## Create appset

```
oc apply -f ocp-gitops/operators-appset.yaml
```