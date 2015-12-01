Set up an Hadoop Development Virtual Machine using Vagrant.

## Install Vagrant

## Install crepo
	git clone https://github.com/cloudera/crepo
	cd crepo
	sudo python setup.py install

## Create VM
	vagrant up

## Get Hadoop
	crepo sync

## Ssh into the VM
	vagrant ssh

## Build Hadoop
In the VM, change directory to "/vagrant/hadoop", and run:

	mvn install -DskipTests -Pdist
