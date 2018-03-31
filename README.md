# ansible-init-env

Prepare a environment before installing Kubernetes.

INSTALL
=======

```
git clone https://github.com/sayya9/ansible-init-env.git
cd ansible-init-env
ansible-playbook --ask-vault-pass init.yml
```

Or skip local yum mirror

```
ansible-playbook --skip-tags mirror --ask-vault-pass init.yml
```
