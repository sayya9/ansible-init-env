# ansible-init-env

Prepare a environment before installing Kubernetes.

INSTALL
=======

```
git clone https://github.com/sayya9/ansible-init-env.git
cd ansible-init-env
ansible-playbook -i inventory/tp-lab01 --ask-vault-pass init.yml
```

Or skip local yum mirror

```
ansible-playbook -i inventory/tp-lab01 --skip-tags mirror --ask-vault-pass init.yml
```

NTP
=======

Update your customer ntp server in roles/geerlingguy.ntp/defaults/main.yml

```
ntp_servers:
  - "0{{ ntp_area }}.pool.ntp.org iburst"
  - "1{{ ntp_area }}.pool.ntp.org iburst"
  - "2{{ ntp_area }}.pool.ntp.org iburst"
  - "3{{ ntp_area }}.pool.ntp.org iburst"
```
