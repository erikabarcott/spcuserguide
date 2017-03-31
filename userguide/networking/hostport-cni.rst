========================================================================
Troubleshooting Kubernetes Networking: HostPort Fails With CNI Plug-In
========================================================================

-----------
Overview
-----------

The `hostPort` pod configuration specifies the port number to expose on the host. This configuration will not work with the `CNI plug-in <https://kubernetes.io/docs/concepts/cluster-administration/network-plugins/#cni>_`. The combination of using `hostPort` and the CNI plug-in will cause Kubernetes to silently ignore the `hostPort` attribute.

This issue is `documented in the official Kubernetes guide <https://kubernetes.io/docs/admin/network-plugins/#cni>`_ and is `being tracked as an open bug <https://github.com/kubernetes/kubernetes/issues/31307>`_. However, this problem is not well-known, and is notorious for causing headaches among users trying to track down the source of a Kubernetes failure.

------------
Workarounds
------------

It should be noted that Kubernetes "best practices" are to `only use `hostPort` when "absolutely necessary" <https://kubernetes.io/docs/concepts/configuration/overview/>`_. The official Kubernetes documentation suggests that users "consider using a `NodePort <https://kubernetes.io/docs/user-guide/services/#type-nodeport>`_ service before resorting to `hostPort`."

Another way around this issue is to use an HAProxy service running on the host network to proxy back into the overlay network, as described in our article `Configure and Manage a Kubernetes HAProxy Ingress Controller <../ingress/haproxy.html>`_.

You may also opt to use a real load balancer to expose services. This process is described in the official Kubernetes documentation under `Creating an External Load Balancer <https://kubernetes.io/docs/tasks/access-application-cluster/create-external-load-balancer/>`_.

-------------
Future Plans
-------------

The ability to use CNI plug-ins is on our feature request list, and may be added in a future update. 

