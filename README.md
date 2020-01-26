# conteco.controlplane.modeco

The `controlplane.modeco` image of the __ContEco__ container ecosystem.
See `conteco.docs.overview` for more information on the ContEco ecosystem.

The `controlplane.modeco` image implements the controlplane for the ModEco ecosystem and is concerned with functional modules.  
The output is a set of modules ready by the ModEco controlplane.  
It provides an full API implementation, inheritance is from `controlplane.base`:
* console - in full, inherited without change
* repo - in full, inherited without change
* config - in full, inherited with added extensions
* build - in full, inherited without change
* release - in full, inherited without change
* deploy - full implementation
* run - full implementation

## Controlplane API

* __console__  
API section containing methods that executes outside the context of a repository.  
Inherited in full from `controlplane.base`.

* __repo__  
API section dealing with version control, GIT based or directly ported from GIT.  
Inherited in full from `controlplane.base`.

* __config__  
API section dealing with repository configuration.  
Inherits implementation from `controlplane.base` with addition of further methods.  
Full implementation - [config API in detail](./docs/CONTROLPLANE-API-CONFIG.md)

* __build__
Build API - container images only.  
Inherited in full from `controlplane.base`.

* __release__  
Release API - container images only.  
Inherited in full from `controlplane.base`.

* __deploy__
Deploy API - of container images, modules or solutions.  
Full implementation - [deploy API in detail](./docs/CONTROLPLANE-API-DEPLOY.md)

* __run__
Run API - of modules or solutions.  
Full implementation - [run API in detail](./docs/CONTROLPLANE-API-RUN.md)

## `controlplane` CLI

`controlplane.conteco` inherits the CLI implementation from `controlplane.base`.  
The scripts to invoke the CLI are extracted from the image to the current folder by:

```bash
# Extracting the CLI instantiation scripts from the controlplane image
docker run -v %cd%:/conteco/pwd vcwebio/conteco.controlplane.base --interactive extract-cli windows # on Windows
docker run -v $(pwd):/conteco/pwd vcwebio/conteco.controlplane.base --interactive extract-cli linux # on linux

# Starting the CLI
# on linux
./start conteco # to start the controlplane for image configuration
./start modeco # to start the controlplane for module management
# on windows
start.bat conteco # to start the controlplane for image configuration
start.bat modeco # to start the controlplane for module management

# Invoking the API
# when conteco CLI is invoked
conteco [API method] [arguments]

# when modeco CLI is invoked
modeco [API method] [arguments]
```

See `conteco.docs.overview` for more information on how to extract and use the commandline interface.
