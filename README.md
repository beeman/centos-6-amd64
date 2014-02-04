centos-6-amd64
=====

My [veewee](https://github.com/jedi4ever/veewee) definitions for CentOS 6 for x86-64. 

You need veewee installed to work with these definitions, [this site](http://cbednarski.com/articles/veewee/) helped me a lot!

Step 1: Checkout the definitions

    $ git clone git@github.com:beeman/centos-6-amd64.git
    $ cd centos-6-amd64

Step 2: Install a new image based on the definitions

    $ veewee vbox build centos-6-amd64 -n
    
Step 3: When the installation is finished you can enter the new image to make changes, exit the SSH session when finished.

    $ ssh -o UserKnownHostsFile=/dev/null -o StrictHostKeyChecking=no -p 7222 -l veewee 127.0.0.1
    
Step 4: Build the vagrant image

    $ veewee vbox export centos-6-amd64
    
Step 5: Use the new image in a Vagrantfile :-)