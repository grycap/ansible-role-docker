[![License](https://img.shields.io/badge/license-Apache%202-blue.svg)](https://www.apache.org/licenses/LICENSE-2.0)
[![CI](https://github.com/grycap/ansible-role-docker/workflows/CI/badge.svg)](https://github.com/grycap/ansible-role-docker/actions?query=workflow%3ACI)

Docker Engine Role
===================

Install Docker Engine (recipe for EC3)

Role Variables
--------------

The variables that can be passed to this role and a brief description about them are as follows.

	docker_mirror_protocol: "http"
	docker_mirror_port: 5000
	docker_opts: ""
	docker_channel: "stable"
	docker_version: "latest"
	# Docker comaptible versions that if are installed docker will not be reinstalled
	# ['17.03.', '18.06.', '18.09.', '19.03.']
	docker_compatible_versions: []
	docker_install_criu: true
	docker_install_pip: true
	docker_compose_version: "1.25.5"
	docker_config_values: {}
	docker_nvidia_support: false
	docker_nvidia_options:
		default-runtime: nvidia
		runtimes:
			nvidia:
				path: /usr/bin/nvidia-container-runtime
				runtimeArgs: []
	# Installs containerd only, not full docker
	docker_containerd_only: false
	docker_containerd_version: 1.6.8
	# Set the version of the command nerdctl to install
	docker_nerdctl_version: 1.0.0
	# Install containerd CNI plugins
	docker_containerd_install_cni: false
	docker_containerd_cni_version: '1.1.1'
	# Set the root path for containerd
	docker_containerd_root: ""

Example Playbook
----------------
```
  - hosts: server
  roles:
  - { role: 'grycap.docker' }
```
```
  - hosts: client
  roles:
  - { role: 'grycap.docker' }
```

Contributing to the role
========================
In order to keep the code clean, pushing changes to the master branch has been disabled. If you want to contribute, you have to create a branch, upload your changes and then create a pull request.  
Thanks
