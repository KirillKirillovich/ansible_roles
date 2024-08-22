# Ansible roles

List of ansible roles, which help you to configure your instances:

1) branch 'ansible_role_docker' - install docker & docker compose on Ubuntu.
Usage:
requirements.yml should contain:
```yml
- src: git+https://github.com/KirillKirillovich/ansible_roles.git
  version: origin/ansible_role_docker
  name: docker
```
```
ansible-galaxy role install -f -r requirements.yml
```

2) branch 'ansible_role_build_image' - Build and push your image to dockerhub.
Usage:
- Override variables in defaults/main.yml
- requirements.yml should contain:
```yml
- src: git+https://github.com/KirillKirillovich/ansible_roles.git
  version: origin/ansible_role_build_image
  name: build_image
```
```
ansible-galaxy role install -f -r requirements.yml
```