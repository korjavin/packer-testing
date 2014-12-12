packer-testing
=============

Packer configuration to generate Debian Testing VirtualBox image/Vagrant boxes.

Usage
-----

To generate a VirtualBox image, edit debian-testing file and adapt the variables fields:
```
    "variables": {
        "debian_version": "7.7.0",
        "iso_checksum": "5cb6e4fea55fbb5173f90c3a545b843c6c193e29c3aa32b3306c9bbdfb1ad6a6a36ae8be50e91af9d03d5f21c472bd05d04d3508172e0b519e76714333c7c74b"
    },

```
You have to set the Debian version and the ISO sha512 checksum. Once done, create your box file:
```
packer build debian-testing
```

This branch has a ansible provisioner which:
 - apply my dotfiles
 - install common soft
 - install docker
