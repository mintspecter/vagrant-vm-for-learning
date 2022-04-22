## Table of content 

* [System requirements](#system-requirements)
* [Recommanded Vagrantfile](#recommanded-vagrantfile)
* [How to use](#how-to-use)
* [Pre-installed](#pre-installed)
* [Change Log](#change-log)

# CentOS-Stream-8-ContainerEnv
Virtual machine for container system training

## System requirements
  * Recommended 
    - CPU: 2 cores or more
    - Memory: 8 GB or more

## Recommanded Vagrantfile

ref: https://github.com/mintspecter/vagrant-vm-for-learning/blob/main/CentOS-Stream-8-ContainerEnv/Vagrantfile
```vagrantfile
Vagrant.configure("2") do |config|
    ## base box
    config.vm.box = "mintspecter/CentOS-Stream-8-ContainerEnv"
    config.vm.box_version = "1.0.0"

    # cockpit  
    config.vm.network "forwarded_port", guest: 9090, host: 19090, protocol: "tcp", auto_correct: true

    # code-serve
    config.vm.network "forwarded_port", guest: 7080, host: 17080, protocol: "tcp", auto_correct: true
  
    # config vm
    config.vm.provider "virtualbox" do |vm|
        vm.memory = "2048" # MB, "2048" is recommended.
        vm.cpus = "2"      # Core, "2" is recommended.
    end
end
```

## How to use
  - English: [https://github.com/mintspecter/vagrant-vm-for-learning/blob/main/CentOS-Stream-8-ContainerEnv/README.en.md](https://github.com/mintspecter/vagrant-vm-for-learning/blob/main/CentOS-Stream-8-ContainerEnv/README.en.md)
  - 한국어: [https://github.com/mintspecter/vagrant-vm-for-learning/blob/main/CentOS-Stream-8-ContainerEnv/README.kr.md](https://github.com/mintspecter/vagrant-vm-for-learning/blob/main/CentOS-Stream-8-ContainerEnv/README.kr.md)

## Pre-installed
  * [cockpit](https://cockpit-project.org/) : Cockpit is a web-based graphical interface for servers
  * [code-server](https://coder.com/): Self-hosted developer workspaces
  * [podman](https://podman.io/): a.k.a [docker](https://www.docker.com/) Podman is a daemonless container engine for developing, managing, and running OCI Containers on your Linux System
  * [podman-compose](https://github.com/containers/podman-compose): a.k.a [docker-compose](https://docs.docker.com/compose/) An implementation of [Compose Spec](https://compose-spec.io/) with Podman backend. 
  * [cockpit-podman](https://github.com/cockpit-project/cockpit-podman) : This is the Cockpit user interface for podman containers.

## Change Log
* 1.0.1 
   - update: code-server port mapping change ; 8080:18080 -> 7080:17080
   - buf-fix: locale settings error
