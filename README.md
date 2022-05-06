## Setup - NFS

For setup the nfs server firstly clone the repo

``` bash
git clone https://github.com/Vortexdude/setup-nf

```
and change to that ansible directory

``` bash
cd setup-nf/ansible
```


And if you want to setup the nfs to the remote change the Host in the playbook [main.yaml](https://github.com/Vortexdude/setup-nfs/blob/main/ansible/main.yaml#L1)
change from `localhost` to your IP `10.0.0.0`

``` yaml

- hosts: localhost
  become: true
  roles:
    - { role: setup-nfs }

```
For change the export directory give the export directory and give the parameter for type of nfs in [default/main.yaml](https://github.com/Vortexdude/setup-nfs/blob/main/ansible/roles/setup-nfs/defaults/main.yaml#L2) and you can change the export directory via `"/mnt/nfs_shares *(rw,sync,no_root_squash,insecure)"` to your any directory `"/folder *(rw,sync,no_root_squash,insecure)"`

``` yaml
nfs_exports: [ "/mnt/nfs_shares *(rw,sync,no_root_squash,insecure)" ]
```

And run the ansible-playbook

``` bash
ansible-playbook main.yaml
```
