Welcome to DevSecOps Studio Project!
=====================================

DevSecOps Studio is one of its kind, self hosted DevSecOps environment to help individuals,professionals in learning DevSecOps concepts. It takes lots of efforts to setup the environment for training/demos and more often, its error prone when done manually. DevSecOps Studio is easy to get started, pre-configured to most extent and used for our Practical DevSecOps Course at https://eracorp.io/devsecops/

DevSecOps Studio project aims to reduce the time to bootstrap the environment and help you in concentrating on learning DevSecOps practices with the below features.

1. Easy to setup environment with few commands
2. Covers Security as Code, Infrastructure as Code
3. With built-in support for CI/CD pipeline, Docker registry (i.e. gitlab)
4. Following environment can be used for Hardening infrastructure using ansible
5. To test compliance as code using Inspec
6. Ability to perform DAST scan using OWASP ZAP
7. Can even run static check tools like bandit, brakeman,trufflehog, gitsecrets, etc.

> **Note:**

> - This repository is used as companion to our [DevSecOps course](https://eracorp.io/devsecops/).

> - Also, the contents in the this repository vary from original repository.

## How do I get set up? ###

* [Summary of setup](#summary-of-setup)
	* [Software](#software)
	* [Hardware](#hardware)
* [Dependencies](#dependencies)
	* [Mac OS X](#macos-optional)
	* [Linux](#linux)
* [DevSecOps Studio Installation](#installation)
* [What's included in the environment](#whats-included-in-the-environment)
* [How to use the setup](#how-to-use-the-setup)
* [Todo Features](#todo-features)
* [Contribution guidelines](#contribution-guidelines)
* [Who do I talk to?](#who-do-i-talk-to)


## Summary of Setup
### TL;DR

Install [Vagrant](https://www.vagrantup.com/downloads.html), [Virtualbox](https://www.virtualbox.org/wiki/Downloads), [Ansible](http://docs.ansible.com/ansible/latest/intro_installation.html#installation) and Follow the below steps.

```bash
# Download the code
$ git clone https://github.com/teacheraio/DevSecOps-Studio.git && cd DevSecOps-Studio

# Download the ansible dependency roles
$ ansible-galaxy install -r requirements.yml -p provisioning/roles

# Setup the environment, takes an hour or less based on your internet speed.
$ vagrant up
```
Go grab some coffee while DevSecOps Studio does its job.

Yes, that's it, you just setup entire DevSecOps environment with three commands :)

Go ahead and read Practical DevSecOps Lessons on the [wiki](https://github.com/teacheraio/DevSecOps-Studio/wiki)

### Details

DevSecOps Studio uses `vagrant`, `virtualbox` and `ansible` to setup the lab environment. You can visit the vendor's website to download the above software for on Windows/Linux/macOS.

DevSecOps Studio simulates the environment presented below.

![](images/appsec-pipeline.png)

### Software

* [Vagrant](https://www.vagrantup.com/downloads.html)
* [Virtualbox](https://www.virtualbox.org/wiki/Downloads)
* [Ansible](http://docs.ansible.com/ansible/latest/intro_installation.html#installation)

### Hardware
* Atleast 8GB of RAM for the virtual machines and 16GB of memory on Host.
* 80GB of HDD Space.
* Intel i3 Processor or above.
* VirtualBox

## Dependencies

### MacOS (optional)

Prerequisites can also be installed via homebrew on MAC OS X

[Homebrew](http://brew.sh/): Optional

```bash
 /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"

```

[Vagrant](https://www.vagrantup.com/downloads.html)

```bash
brew cask install vagrant
```

[Virtualbox](https://www.virtualbox.org/wiki/Downloads)

```bash
brew cask install virtualbox
```

[Ansible](http://docs.ansible.com/ansible/latest/intro_installation.html#installation)

``` bash
brew install ansible
```

### Linux

Install dependencies using apt-get

[Virtualbox](https://www.virtualbox.org/wiki/Downloads)

[Vagrant](https://www.vagrantup.com/downloads.html)

``` bash
sudo apt-get install vagrant python3 python3-pip
```
[Ansible](http://docs.ansible.com/ansible/latest/intro_installation.html#installation)

``` bash
pip install ansible
```
or 

``` bash
sudo apt install ansible
```
You can see how it all fits in DevSecOps pipeline by reading out [WIKI](https://github.com/raghuio/DevSecOps-Studio/wiki)

## How to use the setup

## What's included in the environment?

The environment contains the following tools used in different stages of DevSecOps.

![](images/devsecops-tools.png)

 Technology  | Tools
------------ | -------------
PenTest Toolkit: | Nmap, Nikto
Static Analysis Tools: | bandit
Dynamic Analysis Tools: | ZAP proxy
Hardening: | DevSec Ansible OS Hardening
Operating System :| Ubuntu Jammy (22.04) & Focal Fossa (20.04)
Programming Languages: | Java, Python 2, Python 3, Ruby/Rails
Container Technology:| Docker
Source Code Management:| Gitlab (github like system)
CI Server:| Gitlab CI
Docker Registry:| Gitlab 
Configuration Management:| Ansible
Cloud Provider Utilities:| AWS CLI
Utilities:| Git, Vim, curl, wget,

## Todo Features

- [ ] Provision the stack on AWS using vagrant.
- [ ] Build Images using Packer and upload to vagrant cloud.
- [ ] Add ELK and monitoring setup.
- [ ] Enable Jenkins based pipeline.

## Contribution guidelines

* Fork this repo.
* Contribute (documentation/features)
* Raise a Pull Request (PR)

## Credits

* DevSecOps Studio uses some of the ansible roles from [Jeff](https://github.com/geerlingguy)

* Thanks to Mohammed A. Imran [@secfigo](https://github.com/secfigo) for all valuable contributions and building up DevSecOps studio lab setup.

## Who do I talk to?

* If you have any questions regarding this repo, please contact Raghunath G @raghuio
