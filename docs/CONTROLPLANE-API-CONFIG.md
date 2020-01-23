[`controlplane.conteco`](../README.md) >> `config` API - Full

-----

# `config` API - Full

`controlplane.base` implements the following common methods of the `config` API section:

__`build`__  
Generates the `Dockerfile.static` with the `environment` configuration.  
Should be executed after an update to the variables in the `environment` file.  
The `Dockerfile.static` file allows a direct `docker build` of the image. It is used by the automated Docker Hub build.
Inherited from controlplane.base.

__`module-base`__  
Imports the service stack assets from the ContEco images and stages them for module configuration.  
Module service stacks assets are cloned from the imported assets.

__`module`__  
Configures the module service stacks from the imported ContEco service stacks.  
This includes renaming the stacks using the module specific names.

__`increment`__  [version-part]
Increments the specified version part of a `vx.y.z` version tag in `$CONTECO_TAG`.
Requires $CONTECO_TAG_TYPE=incremental, otherwise action is ignored.
Inherited from controlplane.base.

__`remove-crs`__  
This method remove CRs from files without extension or with _.md_ or _.static_ extension.  
Inherited from controlplane.base.

__`set-version`__  
This method sets the value of the `$CONTECO_TAG` variable.  
Inherited from controlplane.base.

__`volume`__  
Configures the volume initial data states by creating backups of the current state of the volumes.  
Initialised volumes are declared in a separate list.

-----
[`controlplane.conteco`](../README.md) >> `config` API - Full
