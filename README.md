# k8-homework2

### Kubernetes Pod and 'emptyDir' Volume.

An 'emptyDir' volume, as the name suggest, is an empty directory that gets created in the pod. This directory can be shared with pods. Note if the location to which you connect the 'emptyDir' has data, the existing data are masked and become hidden.
* In this example:
A pod named 'nginx-pod' is created.

A label 'app: nginx-app' gets attached to it.

RestartPolicy is set to 'Never', which means the container will not be restarted regardless of why it exited.

Under volumes, it creates 'emptyDir' volume named 'shared-volume'. Which in the background creates an empty folder on the node that the pod gets assigned to. The location of the folder on the node is : /var/lib/kubernetes/pods/< id-of-the-pod >/volumes/kubernetes.io~empty-dir/

Under containers, 2 containers are created.
