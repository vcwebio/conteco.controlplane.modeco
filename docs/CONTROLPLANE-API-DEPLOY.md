[`controlplane.modeco`](../README.md) >> `deploy` API - Full

-----

# `deploy` API - Full

`controlplane.modeco` implements two deployment interfaces, one for the module and one for the named service stacks.  

__`module down`__  
Removes the module deployment from the cluster (network and volumes).  

__`module downup`__  
Removes and redeploys the module to the cluster (network and volumes).  

__`module up`__  
Deploys the module to the cluster (network and volumes).  

__`[stack] down`__  
Removes the service stack(s) and overlay network.  

__`[stack] downup`__  
Restarts the service stack(s).  

__`[stack] up`__  
Deploys the service stack(s) with overlay network and runs it.  

-----
[`controlplane.modeco`](../README.md) >> `deploy` API - Full
