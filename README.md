Set up Hadoop development environment, optonally in a Virtual Machine using Vagrant.

## Set up Hadoop development environment

### Install crepo
	git clone https://github.com/cloudera/crepo.git
	cd crepo
	sudo python setup.py install

### Get Hadoop
Change directory to "hadoop_dev", and run:

	crepo sync

### Build Hadoop
Skip this step if you plan to use a VM. Change directory to "hadoop_dev/hadoop", and run:

	mvn install -Pdist -DskipTests

## (Optional) Create a VM for Hadoop development

### Install Vagrant
Install at least one provider, such as VirtualBox.

### Create VM
	vagrant up

### Ssh into the VM
	vagrant ssh

### Build Hadoop in the VM
Change directory to "/vagrant/hadoop" (Vagrant automaticilly share /vagrant between the guest and the host), and run:

	mvn install -Pdist -DskipTests
