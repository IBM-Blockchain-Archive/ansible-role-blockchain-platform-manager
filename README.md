ansible-role-blockchain-platform-manager
=========

[![Build Status](https://dev.azure.com/IBM-Blockchain/ansible-role-blockchain-platform-manager/_apis/build/status/IBM-Blockchain.ansible-role-blockchain-platform-manager?branchName=master)](https://dev.azure.com/IBM-Blockchain/ansible-role-blockchain-platform-manager/_build/latest?definitionId=1&branchName=master)

Ansible role for managing blockchain networks using the IBM Blockchain Platform.

You can install this role from [Ansible Galaxy](https://galaxy.ansible.com/ibm/blockchain_platform_manager):

`ansible-galaxy install ibm.blockchain_platform_manager`

Requirements
------------

This Ansible role requires the following pre-requisites:
- Python 3.7+
  - https://www.python.org/
- Ansible 2.8+
  - `pip install ansible`
- Hyperledger Fabric binaries (`configtxgen`, `peer`, `fabric-ca-client`, etc)
  - https://hyperledger-fabric.readthedocs.io/en/release-1.4/install.html
- One of the following supported deployment targets:
  - IBM Blockchain Platform on IBM Cloud
  - IBM Blockchain Platform on Red Hat OpenShift (coming soon!)
  - Docker 19.03+
- Docker SDK for Python (if using Docker)
  - `pip install docker`
- `sponge` (from `moreutils`)

Role Variables
--------------

Coming soon!

Dependencies
------------

This Ansible role has no dependencies on any other Ansible roles.

Example Playbook
----------------

Coming soon!

License
-------

Apache-2.0

Author Information
------------------

This Ansible role is maintained by the IBM Blockchain Platform development team. For more information on the IBM Blockchain Platform, visit the following website: https://www.ibm.com/cloud/blockchain-platform
