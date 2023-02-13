# Enterprise Vault 

This repository installs Vault Enterprise version 1.7.1 by using Vagrant. 
# Prerequisites

## License
Make sure you have a Vault Enterprise license available for use

Store this under the directory `files/vault.hclic`

## Vagrant
Vagrant [See documentation](https://www.vagrantup.com/docs/installation)  
Virtualbox [See documentation](https://www.virtualbox.org/wiki/Downloads)

# How to

- Clone the repository to your local machine
```
git clone https://github.com/munnep/vault_enterprise.git
```
- Go to the directory
```
cd vault_enterprise
```
- Place you vault enterprise license under `files/vault.hclic`
- Start the virtual machine
```
vagrant up
```
- Login to vault
```
vagrant ssh
```
- Verify you have a valid Vault running
- Set the following environment variables
```
export VAULT_TOKEN="changeme"
export VAULT_ADDR="http://127.0.0.1:8200"
```
- Output the current status
```
vagrant@vault:~$ vault status
Key             Value
---             -----
Seal Type       shamir
Initialized     true
Sealed          false
Total Shares    1
Threshold       1
Version         1.7.1+ent
Storage Type    inmem
Cluster Name    vault-cluster-7064c150
Cluster ID      a8cdcc20-9dcb-845d-dae7-b6d7e0739342
HA Enabled      false
```
- login to vault
```
vault login changeme
```





