Development notes
=================

These are some misc development notes for collaborators.

## Development: Synchronization to the cluster

You can use ``unison`` to synchronize the source code from local
to the remote cluster. See the script ``unison-to-bigboot1-jbds``.

It is assumed that ``bigboot1`` is the name of the main cluster node,
and that the root directory is ``/data/work/scm/environments/env_jbds/src``.
You need to change these values in the files ``unison-to-bigboot1-jbds``
and ``unison-to-bigboot1-jbds.prf``.

