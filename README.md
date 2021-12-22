# ubuntu-dev-box-with-ansible

## Requisiti
```
sudo apt install git ansible
ansible-galaxy collection install community.general
```

Git clone del progetto

## Confiurazione
- common
    - Upgrade the OS
    - Install programs
        - htop
        - build-essential
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
- snap_dev
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

## Start not dev
```
ansible-playbook site.yml
```

## Start dev
```
ansible-playbook site_dev.yml
```

NOTE:
- oh-my-zsh (con tutti i plugins)
- sdkman
- nvm

Verificare:
- pdfarranger
- flameshot