[![License](https://img.shields.io/badge/license-Apache%202-blue.svg)](https://www.apache.org/licenses/LICENSE-2.0)
[![Build Status](https://travis-ci.org/grycap/ansible-role-ssh.svg?branch=master)](https://travis-ci.org/grycap/ansible-role-ssh)

Docker Engine Role
===================

Install Docker Engine (recipe for EC3)

Example Playbook
----------------
```
  - hosts: server
  roles:
  - { role: 'grycap.docker'}
```
```
  - hosts: client
  roles:
  - { role: 'grycap.docker'}
```

Contributing to the role
========================
In order to keep the code clean, pushing changes to the master branch has been disabled. If you want to contribute, you have to create a branch, upload your changes and then create a pull request.  
Thanks
