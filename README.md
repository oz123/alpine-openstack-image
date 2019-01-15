# alpine-openstack-image
Alpine Linux OpenStack VM Image

## Prerequisites

Install Packer: https://www.packer.io/intro/getting-started/install.html

## Getting Started

```
packer build alpine.json
qemu-img convert -f vmdk -O raw output-virtualbox-iso/alpine38-disk001.vmdk output-virtualbox-iso/alpine38-disk001.raw
openstack image create --file output-virtualbox-iso/alpine38-disk001.raw --disk-format raw --container-format bare alpine38
```
