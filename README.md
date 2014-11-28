# edison-imaging-vm

An Ubuntu 12.04 Vagrant VM (64-bit) for creating custom Intel Edison images.

The VM is provisioned with the essential packages needed to build an Intel Edison image. It is also configured with more memory (i.e. 2GB RAM) and with the ability to connect to Edison via USB (note that Edison may need to be unmounted from the host for it to connect to the VM).

## Prerequisites

* [VirtualBox](https://www.virtualbox.org/)
* [Vagrant](http://www.vagrantup.com/)
* About 30GB of disk space on your host machine

## Setup

### Starting the VM

* To start the VM: `vagrant up`
* To SSH into the VM: `vagrant ssh`
* To navigate to the shared folder: `cd /vagrant`

### Building an Intel Edison image

For details on building Edison images, see this [document from Intel](https://communities.intel.com/docs/DOC-23159).

Click [here](https://communities.intel.com/docs/DOC-23242?_ga=1.216020368.701615573.1414539807) to download the latest Edison Linux Source Files (`.tgz`). If the `.tgz` file is downloaded into the shared folder, it is best to use this command when unpacking the file:

    tar xvf edison-src.tgz -C ~

where `edison-src.tgz` is the name of the downloaded file. `-C ~` unpacks the file into the root directory of the VM. If the source files are in the shared folder, you may run into issues when building an image.