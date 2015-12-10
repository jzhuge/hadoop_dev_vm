Set up Hadoop development environment in a Virtual Machine using Vagrant.
Currently only Ubuntu is supported.

### Install Vagrant
Install at least one provider, such as VirtualBox.

### Create VM
	vagrant up

### Ssh into the VM
	vagrant ssh

### Get Hadoop in the VM
	git clone -o asflive git://git.apache.org/hadoop.git

### Build Hadoop in the VM
	mvn install -Pdist -DskipTests
