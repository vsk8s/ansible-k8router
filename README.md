# k8router

This role configures HAProxy to act as a multi-cluster router. It harddepends on
the `haproxy` role and softdepends on the `router` role, please make sure you
rolled them out before.

### Variables

This role has two mandatory variables, it doesn't make much sense without these.

|Name|Description|
|----|-----------|
|`k8router_ha_group`|The HAProxy peering group this router belongs to. See `defaults/main.yml` for more information. This is used primarily for TLS session resumption.|
|`k8router_k8s_clusters`|A list of Kubernetes clusters to which to route traffic. See `defaults/main.yml` for more information.|
