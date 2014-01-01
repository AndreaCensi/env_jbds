Importing and activating the virtual machine
============================================

The public AMI is called ``ami-abd0e5c2``. 

Copy it to your account as follows:

     $ ec2-copy-image -s ami-abd0e5c2 -r us-east-1
     IMAGE	ami-xxxxxx
     
The output is the new AMI ID.

    $ ec2-run-instance ami-a9d2e7c0 --instance-type cc2.8xlarge
     
     
