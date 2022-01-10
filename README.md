# FreeTAKHub Installation

FreeTAKHub installation is a set of Ansible scripts that allow you to:
- create the target nodes
- install FTS and all the additional modules
- configure FTS

# Install

## PRE-INSTALLATION STEPS: Windows

Currently FreeTAKHub Installation supports Ubuntu 20.04.

To install on Windows, you will have to:

1. Install WSL2.

    See: <https://docs.microsoft.com/en-us/windows/wsl/install>

    See also: <https://www.omgubuntu.co.uk/how-to-install-wsl2-on-windows-10>

    See also: https://www.sitepoint.com/wsl2/

1. Install the WSL Ubuntu 20.04 distribution.

    See: <https://www.microsoft.com/en-us/p/ubuntu-2004-lts/9n6svws3rx71>

### Step 1. Install Ansible and package dependencies

In the Ubuntu console:

```console
sudo apt update
sudo apt install software-properties-common
sudo add-apt-repository --yes --update ppa:ansible/ansible
sudo apt install ansible git
```

See: <https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html#installing-ansible-on-ubuntu>

### Step 2. Clone the FreeTAKHub-Installation Git repository

```console
git clone https://github.com/FreeTAKTeam/FreeTAKHub-Installation.git
```

### Step 3. Install with Ansible

An example default install playbook is defined in: `freetakhub_install.yml`.

This playbook installs all FreeTAKServer and components to your machine.

To execute the default install playbook, from the top directory, enter:

```console
sudo ansible-playbook freetakhub_install.yml
```

# Uninstall

An example default uninstall playbook is defined in: `freetakhub_uninstall.yml`.

The playbook uninstalls all FreeTAKServer and components on your machine.

To execute the default uninstall playbook, from the top directory, enter:

```console
sudo ansible-playbook freetakhub_uninstall.yml
```
