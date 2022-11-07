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
- docker (Only Dev)
    - [github](https://github.com/geerlingguy/ansible-role-docker)
    - [galaxy](https://galaxy.ansible.com/geerlingguy/docker)

- Sdkman (Only Dev)
    - [github](https://github.com/Comcast/ansible-sdkman)
    - [galaxy](https://galaxy.ansible.com/comcast/sdkman)

- NVM (Only Dev)
    - [github](https://github.com/grzegorznowak/ansible-nvm-node)
    - [galaxy](https://galaxy.ansible.com/grzegorznowak/nvm_node)

- oh_my_zsh
    - [github](https://github.com/gantsign/ansible-role-oh-my-zsh)
    - [galaxy](https://galaxy.ansible.com/gantsign/oh-my-zsh)


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
    - Update programs
    - Install programs
        - code
        - keepassxc
        - spotify
        - vlc
        - flameshot
- snap-dev
    - Install programs
        - termius-app
- vscode-extensions
    - Install
        - vscode-icons-team.vscode-icons
        - ms-azuretools.vscode-docker
- docker
- sdkman
- nvm
- oh-my-zsh

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