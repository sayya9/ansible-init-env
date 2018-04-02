# ansible-init-env

Prepare a environment before installing Kubernetes.

INSTALL
=======

To install

```
git clone https://github.com/sayya9/ansible-init-env.git
cd ansible-init-env
ansible-playbook -i inventory/tp-lab01 --ask-vault-pass init.yml
```

Sync yum repos to a local dir

```
ansible-playbook -i inventory/tp-lab01 mirror.yml
```

NTP
=======

Update your customer ntp server in inventory/host_vars/tp-lab01

```
ntp_servers:
  - "0{{ ntp_area }}.pool.ntp.org iburst"
  - "1{{ ntp_area }}.pool.ntp.org iburst"
  - "2{{ ntp_area }}.pool.ntp.org iburst"
  - "3{{ ntp_area }}.pool.ntp.org iburst"
```
