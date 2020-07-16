# The USE Method
## For every resource, check utilization, saturation, and errors.
- resource: all physical server functional components (CPUs, disks, busses, ...)
- utilization: the average time that the resource was busy servicing work 
- saturation: the degree to which the resources has extra work which it can't service, often queued
- errors: the count of error events 

The metrics are usually expressed in the following erms: 
- utilization: as a percent over a time interval, eg, "one disk is running at 90% utilization"
- saturation: as a queue length. eg, "the CPUs have an average run quote length of four"
- errors: scalar counts. eg, "this network interface has ahd fifty late collisions"

## Resource List 
- CPUs: sockets, cores, hardware threads (virtual CPUs)
- Memory: capacity 
- Network interfaces 
- Storage devices: I/O, capacity 
- Controllers: storage, network cards 
- Interconnects: CPUs, memory, I/O 

## Functional Block Diagram 

## Interconnects 

## Metrics 

## Tools Method


