# Overview

## Install Vagrant and VirtualBox

    brew tap caskroom/cask
    brew install brew-cask
    brew cask install vagrant
    brew cask install virtualbox

## Install Ansible

Ansible is the configuration tool we use to describe our servers. To install for development:

    brew install python
    brew install ansible

## Optional to install

Install Vagrant bash completion script.

    brew tap homebrew/completions
    brew install vagrant-completion

## Go!

    ansible-playbook -i inventory/development --private-key ~/.vagrant.d/insecure_private_key -u vagrant openconext.yml
