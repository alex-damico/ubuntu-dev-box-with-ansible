# ubuntu-dev-box-with-ansible

## Requirements
```
sudo apt install git ansible
```

Git clone: https://github.com/alex-damico/ubuntu-dev-box-with-ansible.git

## Install roles and collections
```
ansible-galaxy collection install -r requirements.yml
ansible-galaxy role install -r requirements.yml
```

NOTE:
- Sdkman (Only Dev)
    - [github](https://github.com/Comcast/ansible-sdkman)
    - [galaxy](https://galaxy.ansible.com/comcast/sdkman)

- NVM (Only Dev)
    - [github](https://github.com/grzegorznowak/ansible-nvm-node)
    - [galaxy](https://galaxy.ansible.com/grzegorznowak/nvm_node)

- antigen
    - [github](https://github.com/gantsign/ansible_role_antigen)
    - [galaxy](https://galaxy.ansible.com/gantsign/antigen)


## Configuration
- common
    - Upgrade the OS
    - Remove dependencies that are no longer required
    - Install programs
        - htop
        - build-essential
        - net-tools
        - git
        - pdfarranger
        - gparted
        - gitg
- google-chrome
    - install google-chrome
- snap
    - Install programs
        - code
        - keepassxc
        - spotify
        - vlc
        - flameshot
- snap-dev
    - Update programs
    - Install programs
        - termius-app
- vscode-extensions
    - Install
        - vscode-icons-team.vscode-icons
        - ms-azuretools.vscode-docker
- docker-compose
    - Install docker-compose
- docker-users
    - enable user 
- sdkman
- nvm
- antigen (oh-my-zsh)

## Start not dev
```
ansible-playbook site.yml
```

## Start dev
```
ansible-playbook site_dev.yml
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

https://galaxy.ansible.com/geerlingguy/docker
