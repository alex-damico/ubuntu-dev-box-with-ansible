# ubuntu-dev-box-with-ansible

## Requirements
```
sudo apt install git ansible
ansible-galaxy collection install community.general
```

Git clone del progetto

NOTE (Only Dev):
- Sdkman
    - [github](https://github.com/Comcast/ansible-sdkman)
    - [galaxy](https://galaxy.ansible.com/comcast/sdkman)
```
ansible-galaxy install comcast.sdkman
```
- NVM
    - [github](https://github.com/grzegorznowak/ansible-nvm-node)
    - [galaxy](https://galaxy.ansible.com/grzegorznowak/nvm_node)
```
ansible-galaxy install grzegorznowak.nvm_node
```
- oh-my-zsh
    - [github](https://github.com/gantsign/ansible-role-oh-my-zsh)
    - [galaxy](https://galaxy.ansible.com/gantsign/oh-my-zsh)
```
ansible-galaxy install gantsign.oh-my-zsh
```
- antigen (feature)
    - [github](https://github.com/gantsign/ansible_role_antigen)
    - [galaxy](https://galaxy.ansible.com/gantsign/antigen)
```
ansible-galaxy install gantsign.antigen
```

## Configuration
- common
    - Upgrade the OS
    - Install programs
        - htop
        - build-essential
        - net-tools
        - git
        - pdfarranger
- google-chrome
    - install google-chrome
- snap
    - Install programs
        - code
        - keepassxc
        - spotify
        - vlc
        - libreoffice
        - flameshot
- snap-dev
    - Install programs
        - docker
        - termius-app
        - postman
        - intellij-idea-community
- vscode-extensions
    - Install
        - vscode-icons-team.vscode-icons
        - ms-azuretools.vscode-docker
- docker-compose
    - Install docker-compose
- docker-users
    - enable user 
- Sdkman
- nvm

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

NOTE:
- oh-my-zsh (con tutti i plugins)
