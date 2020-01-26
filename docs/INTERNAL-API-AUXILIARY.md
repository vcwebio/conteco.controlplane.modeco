[`controlplane.modeo`](../README.md) >> API Auxiliary Methods

-----

# API Auxiliary Methods

## `/conteco/bin`

__`modeco`__  
Entrypoint for the API when called from the CLI.

## `/conteco/bin/controlplane/internal`

__`.modeco`__  
Entrypoint for the API if called as a base API from a derived controlplane.

## `/conteco/bin/controlplane/modeco/internal`

This folder contains auxiliary methods supporting the implementation of the `config` API.

__`config-module`__  
Auxiliary method to configure the module service stacks from the assets imported from the ContEco images.  
This includes renaming the service stack with the module specific names.

__`config-module-base`__  
Auxiliary method to import the service stack assets from the ContEco images.

__`config-volume`__  
Auxiliary method to backup the current data state of the volumes flagged as initialised.

__`config-deploy-module-down`__  
Auxiliary method to remove the deployment of the module (network and volumes).

__`config-deploy-module-up`__  
Auxiliary method to deploy the module (network and volumes).

__`deploy-up`__  
Generates the actual docker-compose.yml file applying the _environment_ non global settings and starts the service stack.

-----
[`controlplane.modeco`](../README.md) >> Auxiliary API
