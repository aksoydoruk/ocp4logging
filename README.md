# OCP4 LOGGING

Needded YAML files for Openshift 4 Logging

###Install the Elasticsearch Operator using the CLI###

1- Create the Namespace:
oc create -f eo-namespace.yaml

2-Create an Operator Group object:
oc create -f eo-og.yaml

3-Create the Subscription object:
oc create -f eo-sub.yaml

4-Change to the openshift-operators-redhat project:
oc project openshift-operators-redhat

5-Create the RBAC object:
oc create -f eo-rbac.yaml

6-Verify the Operator installation:
oc get csv --all-namespaces

###Install the Cluster Logging Operator using the CLI###

1-Create the Namespace:
oc create -f clo-namespace.yaml

2-Create the OperatorGroup object:
oc create -f clo-og.yaml

3-Create the Subscription object:
oc create -f clo-sub.yaml

4-Verify the Operator installation.
oc get csv --all-namespaces

5-Create the instance:
oc create -f clo-instance.yaml

oc get pods -n openshift-logging

