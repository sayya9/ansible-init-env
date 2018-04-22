# ansible-init-env

Prepare a environment before installing Kubernetes.

INSTALL
=======

To clone

```
git clone https://github.com/sayya9/ansible-init-env.git
cd ansible-init-env
cp -a inventory/example inventory/your_host
```

To modify

```
inventory/your_host/*
```

To install

```
ansible-playbook -i inventory/your_host/inventory -b --ask-vault-pass init.yml
```

Sync yum repos to a local dir

```
ansible-playbook -i inventory/your_host/inventory -b mirror.yml
```

Variables
=======

Update your customer ntp servers in inventory/your_host/group_vars/all.yml

```
ntp_servers:
  - "0{{ ntp_area }}.pool.ntp.org iburst"
  - "1{{ ntp_area }}.pool.ntp.org iburst"
  - "2{{ ntp_area }}.pool.ntp.org iburst"
  - "3{{ ntp_area }}.pool.ntp.org iburst"
```

Update your kubeconfig users in inventory/your_host/group_vars/all.yml

```
kube_users:
  - inu
  - andrew
```
