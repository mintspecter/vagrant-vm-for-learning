## Table of contents

* [CentOS-Stream-8-ContainerEnv](#CentOS-Stream-8-ContainerEnv)
* [Usage](#Usage)
  * [1. Initialize virtual machine](#1.-Initialize-virtual-machine)
  * [2. Access to virtual machine](#2.-Access-to-virtual-machine)
    * [Cockpit](#Cockpit)
    * [Code-server a.k.a Visual Studio Code](#Code-server-a.k.a-Visual-Studio-Code)

# CentOS-Stream-8-ContainerEnv

Virtual machine for container system training

  * Recommended system requirements
    - CPU: 2 cores or more
    - Memory: 8 GB or more

  * How to use
    - English: [README.en.md](README.en.md)
    - 한국어: [README.kr.md](README.ko.md)

  * The following environments are pre-installed.
    * [cockpit](https://cockpit-project.org/) : Cockpit is a web-based graphical interface for servers
    * [code-server](https://coder.com/): Self-hosted developer workspaces
    * [podman](https://podman.io/): a.k.a [docker](https://www.docker.com/) Podman is a daemonless container engine for developing, managing, and running OCI Containers on your Linux System
    * [podman-compose](https://github.com/containers/podman-compose): a.k.a [docker-compose](https://docs.docker.com/compose/) An implementation of [Compose Spec](https://compose-spec.io/) with Podman backend. 
    * [cockpit-podman](https://github.com/cockpit-project/cockpit-podman) : This is the Cockpit user interface for podman containers.

## Usage

### 1. Initialize virtual machine
   * install [virtualbox](https://www.virtualbox.org/)
   * install [vagrant](https://www.vagrantup.com/)
   * clone this repository 
     ```
     git clone https://github.com/mintspecter/vagrant-vm-for-learning.git
     cd ./CentOS-Stream-8-ContainerEnv
     ```
   * and vagrant up
     ```
     vagrant up --provider=virtualbox
     ```
### 2. Access to virtual machine

#### Cockpit

1. Access the following URL in your browser
   - URL: https://localhost:19090 or https://YOUR-HOSTNAME:19090
	  
2. Enter user ID and password
   - ID: vagrant
   - PW: vagrant

#### Code-server a.k.a Visual Studio Code

1. Access the following URL in your browser
   - URL: https://localhost:17080 or https://YOUR-HOTNAME:17080

2. Enter password
   - PW: vagrant
