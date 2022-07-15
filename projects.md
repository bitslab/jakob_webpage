---
layout: default.njk
name: Jakob Eriksson
title: Assoc. Professor
---

# Compound Processes

Modern computer software commonly consists of groups of programs executing together. This may be as simple as a web server and a database, or as complex as thousands of virtual machines, each running dozens of programs, all working together toward the same goal. Such groups of related programs are often started by a single user, who may even think of them as a single unit or “stack". Today, this common model of a stack of software, working toward a single goal on behalf of a single user is not reflected in the way the software actually executes. Instead, each individual layer of the stack is painstakingly guarded against incursion by other layers, through a mechanism called process isolation. What’s more, many modern stacks consist of groups of virtual machines (VMs), where an additional layer of safeguards is imposed between VMs, often resulting in high overheads and low efficiency. 

This project introduces a new concept, a “compound process” which better reflects the realities of modern software. A compound process may host several “guest” programs in a single trust domain, eliminating expensive and often redundant safeguards between components of a single software stack, to yield substantial performance benefits. 

# Efficient Multi-Threading with Trust<T> 

Trust<T> is a Rust-based message-passing framework which aims to replace locking and shared memory with a form of message passing called _delegation_. 
With Trust<T>, any shared objects are _entrusted_ to a single core, and accessed via message passing to this core only. 
This ensures race-freedom on the object, eliminates lock contention, and dramatically constrains opportunities for false sharing. 

# Rackwide Computing

Building on Trust<T> and its elimination of shared memory computing, Rackwide Computing is the idea that we can program against an entire rack of computers as if it was a single one. With Rackwide computing, we use Trust<T> delegation over RDMA to create a programming framework that seamlessly scales programs to run across multiple machines. In essence, a single _process_ may span an entire rack. 