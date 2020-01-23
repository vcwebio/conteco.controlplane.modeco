[`controlplane.conteco`](../README.md) >> `run` API - Full

-----

# `run` API - Full

The run interface splits the service stacks in two categories - core services and others.

_boot_ and _shutdown_ are used to deploy / remove service stacks that require to be
up and running prior to starting the processing / ui functions of the module.

_start_ and _stop_ are used to deploy / remove processing and UI service stacks plus other ancillary services.

`controlplane.modeco` implements the following methods for the `run` API section:  

__`boot`__ [stack - optional]  
Starts the service stacks registered as boot stacks.
Boot service stacks need to be up and running before the module can be started.  

__`pause`__ [stack - optional]  
Pauses a service stack. This can be any service stack of the module.  

__`reboot`__ [stack - optional]  
Restarts the service stacks registered as boot stacks.
Boot service stacks need to be up and running before the module can be started.  

__`restart`__ [stack - optional]  
Restarts the service stacks registered as run stacks.
Run stacks implement the dynamic functionality of the module.  

__`resume`__ [stack - optional]  
Resumes a service stack. This can be any service stack of the module.  

__`shutdown`__ [stack - optional]  
Shuts down the service stacks registered as boot stacks.
Boot service stacks need to be up and running before the module can be started.  

__`start`__ [stack - optional]  
Starts the service stacks registered as run stacks.
Run stacks implement the dynamic functionality of the module.  

__`stop`__ [stack - optional]  
Stops the service stacks registered as run stacks.
Run stacks implement the dynamic functionality of the module.  

-----
[`controlplane.conteco`](../README.md) >> `run` API - Full
