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






















# vagrant-vault-ent-download
download ent vault



vagrant@vault:~$ vault status
Error checking seal status: Get "https://127.0.0.1:8200/v1/sys/seal-status": http: server gave HTTP response to HTTPS client
vagrant@vault:~$ export VAULT_ADDR="http://127.0.0.1:8200"
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
Cluster Name    vault-cluster-5d6e592d
Cluster ID      94154a26-155e-225d-a778-a71535385144
HA Enabled      false

export VAULT_TOKEN="changeme"


vault login changeme
WARNING! The VAULT_TOKEN environment variable is set! This takes precedence
over the value set by this command. To use the value set by this command,
unset the VAULT_TOKEN environment variable or set it to the token displayed
below.

Success! You are now authenticated. The token information displayed below
is already stored in the token helper. You do NOT need to run "vault login"
again. Future Vault requests will automatically use this token.

Key                  Value
---                  -----
token                changeme
token_accessor       oERdpzdSO5b8ROxl4Ew1YBoY
token_duration       ∞
token_renewable      false
token_policies       ["root"]
identity_policies    []
policies             ["root"]


