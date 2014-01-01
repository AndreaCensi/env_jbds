Importing and activating the virtual machine
============================================

The public AMI is called ``ami-abd0e5c2``. 

Method 1: Running the AMI directly
-----------------------------------

     $ ec2-run-instance ami-a9d2e7c0 --instance-type c3.large
     

Method 2: Copying the AMI to your account
---------------------------------------------

You can also copy the AMI and inspect the volume snapshots.

Copy it to your account as follows:

     $ ec2-copy-image -s ami-abd0e5c2 -r us-east-1
     IMAGE	ami-xxxxxx
     
The output is the new AMI ID.

    $ ec2-run-instance ami-xxxxxx --instance-type cc2.8xlarge
    
    
     
Troubleshooting
===============

**Cannot ``ssh`` into the machine**

Probably the "security group" does not allow SSH connections. 

     
