# Uniqa Ansible Repo
## Install Packages

```bash
ansible-galaxy install geerlingguy.clamav
ansible-galaxy install softasap.sa-secure-audit-rkhunter
ansible-galaxy install maxlareo.chkrootkit
ansible-galaxy install gantsign.pwquality
```

## Sudo Check

```bash
ansible-playbook -i ansible_inventory sudocheck.yml
```

## Create users

```bash
ansible-playbook --extra-vars '@secret.yml' -i inventory --ask-vault-pass create-users.yml
```

## Deploy security

```bash
ansible-playbook --extra-vars '@secret.yaml' -i inventory --ask-vault-pass ansible-server-security.yaml
```

```bash
ansible-playbook --extra-vars '@secret.yaml' -i inventory --ask-vault-pass ansible-server-antivirusscan.ansible.yml
```

## Deploy Vector

```bash
ansible-playbook --extra-vars '@secret.yml' -i inventory --ask-vault-pass vector.yaml
```
# ansible-testing-repo
