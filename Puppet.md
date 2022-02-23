# Puppet

## What is Puppet?
- open-source IT automation tool
- Ruby-based programming language that provides a precise and adaptable way to describe a desired state for each machine
- you describe the final state, Puppet gets your machines in that state
- declarative

## Features
- Idempotency
- Cross-platform
    - Resource Abstraction Layer (RAL)

## Resources
- fundamental unit for modeling system configurations
- smallest building block of Puppet language
    - singular element you wish to evaludate/create/remove
- Puppet comes w/many builtin resources to manipulate system components you are already familiar with, e.g.,
    - user
    - group
    - file
    - package
    - service
    - exec
    - notify
- block of Puppet code descriding a resource is a resource declaration
- resources can be combined to represent the desired state of your system
- use puppet to implement this manifest (note: we don't "run" the manifest)

## Resource Abstraction Layer (RAL)
- RAL splits resources into types and providers
- providers are the interface between the underlying OS and the resource types

## puppet resource
- command-line tool for inspecting resources on you system
- interacts directly with RAL to get the job done

## Implementing a Manifest
Puppet will
- use dependency info (if supplied) to determine which resources should be handles first
- compile manifest into a Puppet catalog (JSON)
- evaluate each resource to determine if changes are necessary
- create, modify, or remove the resource (if needed) to achieve the desired state
- provide verbose feedback about each resource, i.e., whether it changed and what was done to change it
- log/text/slack/IRC/Twitter/Splunk/etc. results

## Managing Files
- the file resource allows us to manage files

## Classes
- define a collection of resources that are managed together as a single unit
- defining a class makes it available, but does not declare it (i.e., it isn't used/applied)
- classes are singletons (vs. resources, where there are many)

## Modules
- modules are self-contained bundles of code and data
- all Puppet manifests belong in modules (except site.pp)
- you can download pre-built modules from the Puppet Forge or you can write your own
- teh only way Puppet can find (and load) classes is if they are in modules