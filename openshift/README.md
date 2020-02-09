# Install in Openshift 4.x

```
$ oc create -f qemu-ga.yml
$ oc adm policy add-scc-to-user privileged -n qemu-ga -z qemu-ga
```
or
```
oc adm policy add-scc-to-user restricted-sysctls -z qemu-ga
oc adm policy add-scc-to-user privileged -z qemu-ga
oc adm policy add-scc-to-user hostaccess -z qemu-ga
oc adm policy add-scc-to-user hostnetwork -z qemu-ga

```
