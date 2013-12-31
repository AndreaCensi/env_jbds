README for EBS volume 1307-ws-jbds
----------------------------------

This volume contains source code, datasets, and results output, for the paper
"Bootstrapping bilinear models of simple Vehicles". 

The main page for the paper is <http://purl.org/censi/2013/jbds>
where you can find further materials and explanations.

Contents of this volume:

- The directory ``boot-datasets`` contains the datasets.
- The directory ``env_jbds`` contains the source code and a Python environment
  (in deploy/) with all software preinstalled
- The directory ``workspace`` contains the results of the computation.

To reproduce the results:

1. Activate the virtual environment:

    cd /1307-ws-jbds/env_jbds
    source environment.sh

2. Run the command ``yc jbds``:
    
    cd /1307-ws-jbds/workspace
    nice -n 20 yc jbds -c "parmake"

Alternatively, using

    yc jbds --console

gives you a [Compmake][compmake] prompt.



[compmake]: http://compmake.org/





