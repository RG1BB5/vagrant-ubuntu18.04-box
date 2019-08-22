# vagrant-ubuntu18.04-box
A Packer config and setup scripts for building a Vagrant Ubuntu18.04 box

## Install requirements
- Vagrant - [https://www.vagrantup.com/docs/installation/](https://www.vagrantup.com/docs/installation/)
- Packer - [https://www.packer.io/intro/getting-started/install.html](https://www.packer.io/intro/getting-started/install.html)

## To build the vagrant box file
    packer build packer_ubuntu18_04.json

## To add the local box file to vagrant
    vagrant box add ubuntu18_04 build/ubuntu18_04.box

## Alternatively
You can use vagrant cloud to install the latest version without having to build the box file manually, all you have to do is add the following line to your Vagrantfile.

    config.vm.box = "RG1BB5/ubuntu18_04"

Or you can initialiaze it using the Vagrant init command.

    vagrant init RG1BB5/ubuntu18_04 --box-version 0.0.1

## To remove the box from vagrant
    vagrant box remove ubuntu18_04

Example Vagrantfile can be found in the example directory.
