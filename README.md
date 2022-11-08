# ubuntu-dev-box-with-ansible

## Requirements
```
sudo apt install git ansible
```

Git clone: https://github.com/alex-damico/ubuntu-dev-box-with-ansible.git

## Install roles and collections
```
ansible-galaxy collection install -r requirements.yml
```
```
ansible-galaxy role install -r requirements.yml
```

NOTE:
- oh-my-zsh
    - [github](https://github.com/gantsign/ansible-role-oh-my-zsh)
    - [galaxy](https://galaxy.ansible.com/gantsign/oh-my-zsh)
    
- docker (Only Dev)
    - [github](https://github.com/geerlingguy/ansible-role-docker)
    - [galaxy](https://galaxy.ansible.com/geerlingguy/docker)

- Sdkman (Only Dev)
    - [github](https://github.com/Comcast/ansible-sdkman)
    - [galaxy](https://galaxy.ansible.com/comcast/sdkman)

- jet-brains-toolbox (Only Dev)
    - [github](https://github.com/webarchitect609/ansible-role-jet-brains-toolbox)
    - [galaxy](https://galaxy.ansible.com/webarchitect609/jet_brains_toolbox)


## Configuration
- common
    - Upgrade the OS
    - Remove dependencies that are no longer required
    - Install programs (see default file)
- common-folder
    - create folder (see default file)
- google-chrome
    - install google-chrome
- snap
    - Update programs
    - Install programs (see default file)
- snap-dev
    - Install programs (see default file)

- vscode-extensions
    - Install extensions (see default file)
- nvm-node
    - Install nvm and node (default: node 18.12.0)
- docker
- sdkman
- oh-my-zsh
- oh-my-zsh-plugins
    - Download plugin custom (see default file)

## Start not dev
```
ansible-playbook site.yml
```

## Start dev
```
ansible-playbook site_dev.yml
```

## Start dev for work (virtual machines)
```
ansible-playbook site_dev_work.yml
```

## Example override
```
---
- hosts: localhost
  roles:
    - role: common
      base:
      - filezilla
```