# Drupal Melbourne Box

## Requirements

[Packer](https://packer.io/downloads.html) *also available in homebrew

## Test Build 

```
packer push -name DrupalMel/box-dev template.json
```

## Build new release 

```
packer push -name DrupalMel/box template.json
```

## Vagrant

An example vagrant config is provided -- https://github.com/drupalmel/packer-templates/tree/master/ubuntu-12.04-x86_64/example

Only ```Vagrantfile``` & ```vagrant.box.yml``` are required.

To override the box config copy/rename vagrant.ansible.yml.default to vagrant.ansible.yml and update as required.

Changes made to this file are only applied during the initial vagrant up or when you run ```vagrant provision```

No provisioning will occur if vagrant.ansible.yml doesn't exist. 