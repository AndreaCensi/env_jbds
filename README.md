# Bootstrapping Bilinear Models of Simple Vehicles - source code and datasets

This repository contains the source code and datasets 
for the paper  *Bootstrapping Bilinear Models of Simple Vehicles*
(in the spirit of *reproducible research*).
The paper's PDF, slides, and other additional materials are found 
[on this webpage][webpage].

[webpage]: http://purl.org/censi/2013/jbds

After a few years of experience I realized that the best way 
to disseminate the computational elements of research 
are to disseminate them as a virtual machine. Currently, Amazon EC2
is the best platform for the job.


## Instructions for running code from the Amazon cloud

These are instructions that allow to clone our virtual machine setup
on your own Amazon EC2 account.

1. Import and activate the Amazon EC2 virtual machine.
2. Login to the virtual machine.
3. Run the experiments.

### Step 1: Importing and activating the virtual machine


The public AMI is called ``ami-abd0e5c2``. 

#### Method 1: Running the AMI directly

     $ ec2-run-instance ami-abd0e5c2 --instance-type c3.large
     

#### Method 2: Copying the AMI to your account

You can also copy the AMI and inspect the volume snapshots.

Copy it to your account as follows:

     $ ec2-copy-image -s ami-abd0e5c2 -r us-east-1
     IMAGE	ami-xxxxxx
     
The output of the command is the new AMI ID (here indicated as ``ami-xxxxx``).

    $ ec2-run-instance ami-xxxxxx --instance-type cc2.8xlarge
    
### Step 2: Login to the virtual machine

The username is ``researcher`` and the password is ``rr``.

Look up the IP on the AWS Console and simply ssh into it.


#### Troubleshooting

**Cannot ``ssh`` into the machine**. Most likely the "security group" you chose (or the default for your account)  does not allow SSH connections. Don't overthink this error.

If the security group is correct, then look at the virtual machine's console output from the AWS console.


### Step 3: Run the experiments

Assuming that everything was fine, the following will do:

    cd /1307-ws-jbds/env_jbds
    source environment.sh
    cd /1307-ws-jbds/workspace
    nice -n 20 yc jbds -c "parmake"

[See here for a longer explanation.](README-1307-ws-jbds.md).


## Instructions for reproducing the development environment from scratch

[See here for instructions on how to setup the development environment from scratch](README-development.md).
