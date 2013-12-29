# Bootstrapping Bilinear Models of Simple Vehicles

This repository contains the source code and datasets 
for the paper  *Bootstrapping Bilinear Models of Simple Vehicles*
(in the spirit of *reproducible research*).
The paper's PDF, slides, and other additional materials are found 
[on this webpage][webpage].

[webpage]: http://purl.org/censi/2013/jbds

## Introduction

After a few years of experience I realized that the best way 
to disseminate the computational elements of research 
are to disseminate them as a virtual machine. Currently, Amazon EC2
is the best platform for the job.

These are instructions that allow to clone our virtual machine setup
on your own Amazon EC2 account.

(**to finish**)



## Running

Once all the data logs are installed, you can do:

    nice -n 10 yc jbds-estimation-figures -c "parmake" 
    nice -n 10 yc jbds-estimation-fraction -c "parmake" 
    nice -n 10 yc jbds-videos-navigation -c "parmake" 
    nice -n 10 yc jbds-videos-servo -c "parmake" 

The first one might take a long time to execute and occupy lots of space.
On current machines, ``yc jbds-estimation-figures`` takes 13 cpu-days
and occupies 21GB of space.


## Development: Synchronization to the cluster

You can use ``unison`` to synchronize the source code from local
to the remote cluster. See the script ``unison-to-bigboot1-jbds``.

It is assumed that ``bigboot1`` is the name of the main cluster node,
and that the root directory is ``/data/work/scm/environments/env_jbds/src``.
You need to change these values in the files ``unison-to-bigboot1-jbds``
and ``unison-to-bigboot1-jbds.prf``.

