# My Homelab Infra

A repository to setup my Pi homelab using Ansible & k3s.

All code is originally from https://github.com/k3s-io/k3s-ansible with changes to fit my configuration. 

## Instructions
* Build a Pi base image using the Raspbery Pi Imager
  * I used Raspberry Pi OS Lite 64 bits
  * Remember the settings to allow SSH access, public key authentication & to set the hostname
* Ensure the Ansible hosts are correct locally. See `hosts.bak` for the last version I saved
* Provision the cluster using:
    ```shell
    ansible-playbook site.yml -i inventory/personal/hosts.ini
    ```