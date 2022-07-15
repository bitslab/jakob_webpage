---
name: Prof. Jakob Eriksson
title: Recent Rust enthusiast
---

# Some Current Research Projects

Below is a sampling of current research projects we are pursuing in my group. I am always open to exploring new ideas, so if you have something you are passionate about, and which you think I can advise you effectively on, then by all means get in touch!

# Compound Processes
_with Nilanjana Basu_ 
Modern computer software commonly consists of groups of individual programs working together toward the same goal. This *common purpose* model is not reflected in the way the software actually executes today. Instead, each program runs in carefully guarded isolation, communicating via secure system calls. This project introduces a new concept, a “compound process” which better reflects the realities of modern software. A compound process may host several “guest” programs in a single trust domain, eliminating expensive and often redundant safeguards between components of a single software stack, to yield substantial performance benefits. 

# Efficient Multi-Threading with Trust<T> 
_with Ben Baenen_

Trust<T> is a Rust-based message-passing framework which aims to replace locking and shared objects with a particularly efficient form of message passing. 
With Trust<T>, a shared object is _entrusted_ to a single core, which is responsible for all accesses to this object. 
This ensures race-freedom on the object, eliminates lock contention, and dramatically constrains opportunities for false sharing, often resulting in dramatically higher performance. 

# Rackwide Computing
_with Noaman Ahmad_

Building on Trust<T> and its elimination of shared memory computing, Rackwide Computing is the idea that we can program against an entire rack of computers as if it was a single one. With Rackwide computing, we use Trust<T> delegation over RDMA to create a programming framework that seamlessly scales programs to run across multiple machines. In essence, a single _process_ may span an entire rack, allowing (mostly) normal programs to scale to thousands of cores, without the complexities and inefficiencies of cluster computing. 