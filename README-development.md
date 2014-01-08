Development notes
=================

## Step 1: Checkout the source code

The file ``resources.yaml`` lists all necessary repositories.

If you installed ``patience`` (``sudo pip install patience``) then this should suffice:
    
    $ pat checkout -s -v
    
Otherwise, you can just use ``git`` manually.

## Step 2: Initialize the environment

Use the script ``initialize_environment.sh`` to install a virtual environment in ``deploy/``:

    $ ./initialize_environment.sh
    
This creates the file ``environment.sh`` with all necessary configuration. From now on, you need to activate the environment:

    $ source environment.sh

## Step 3: Install the Python packages in the environment

Using ``patience`` you can do:

    $ pat develop -s -v
   
Otherwise, go through the repositories in the order they are listed in ``resources.yaml`` 
and run:

    $ python setup.py develop
   
## Step 4: Additional special instructions 

Some packages require an extra step.

### ``vehicles``

Install the raytracer:

    $ cd src/vehicles/src/raytracer
    $ ./install.sh



## Synchronization to the cluster using Unison

You can use ``unison`` to synchronize the source code from local
to the remote cluster. See the script ``unison-to-bigboot1-jbds``.

It is assumed that ``bigboot1`` is the name of the main cluster node,
and that the root directory is ``/data/work/scm/environments/env_jbds/src``.
You need to change these values in the files ``unison-to-bigboot1-jbds``
and ``unison-to-bigboot1-jbds.prf``.

