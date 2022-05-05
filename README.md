# setup-nfs

#### Role Variables
Available variables are listed below, along with default values (see `/defaults/main.yml`):

nfs_exports: [ "/mnt/nfs_shares *(rw,sync,no_root_squash)" ]

#### Clone the repo
``` bash
git clone https:/github.com/vortexdude/setup-nfs

```

#### Go to the ansible directory

``` bash

cd setup-nfs/ansible

```
#### setup the ip of the address in `inventory/all`

``` bash

[all]
localhost 

```
> You can change the `localhost` to you ipaddres `10.0.0.0`


#### Run the playbook

``` bash

ansible-playbook main.yaml

```
