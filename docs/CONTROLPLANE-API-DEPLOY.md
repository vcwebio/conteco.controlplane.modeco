[`controlplane.modeco`](../README.md) >> `deploy` API - Full

-----

# `deploy` API - Full

`controlplane.modeco` implements two deployment interfaces, one for the module and one for the named service stacks.  

__`down/downup/up [stack]`__  
Removes, removes and deploys, and deploys the module deployment from the cluster (network and volumes).  
It invokes the equivalent local- method as a global service to manage the volumes on each node.

__`local-down/local-downup/local-up [stack]`__  
Removes, removes and deploys, and deploys the module deployment from the cluster (volumes on a node).  

-----
[`controlplane.modeco`](../README.md) >> `deploy` API - Full
