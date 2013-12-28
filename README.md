






Once all the data logs are installed, you can do:

    nice -n 10 yc jbds-estimation-figures -c "parmake" 
    nice -n 10 yc jbds-estimation-fraction -c "parmake" 
    nice -n 10 yc jbds-videos-navigation -c "parmake" 
    nice -n 10 yc jbds-videos-servo -c "parmake" 

The first one might take a long time to execute and occupy lots of space.
On current machines, ``yc jbds-estimation-figures`` takes 13 cpu-days
and occupies 21GB of space.


## Synchronization to the cluster

You can use ``unison`` to synchronize the source code from local
to the remote cluster. See the script ``unison-to-bigboot1-jbds``.

It is assumed that ``bigboot1`` is the name of the main cluster node,
and that the root directory is ``/data/work/scm/environments/env_jbds/src``.
You need to change these values in the files ``unison-to-bigboot1-jbds``
and ``unison-to-bigboot1-jbds.prf``.

