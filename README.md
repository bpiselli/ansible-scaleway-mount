# ANSIBLE mount full

Ansible script to mount additional volume no your server

This role can be used as a dependency of other roles to easily mount additional volume.   
It has initially been built for [Scaleway cloud services](https://www.scaleway.com) but can be used for any mouting purpose. 

### Installation

This role requires at least Ansible `v2.0.0`. To install it, run:

    ansible-galaxy install bpiselli.cloud-mount

### Role Variables

You can simply list all the mounts you'll need

    cloud_mounts:
      - source: '/dev/nbd1'
        destination: '/mnt/data'
        fstype: 'ext4'
      - source: '/dev/nbd2'
        destination: '/mnt/log'
        fstype: 'ext4'


### Authors and license

`scaleway-mount` role was written by:
- Bertrand Piselli | [GitHub](https://github.com/bpiselli)

License: [GPLv3](https://tldrlegal.com/license/gnu-general-public-license-v3-%28gpl-3%29)