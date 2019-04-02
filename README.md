# redhat
Repositorio para deployment de RedHat

![provisioning architecture](iac.png?raw=true "Infrastructure as a Code")

## create password vault to encrypt password

```
ansible-vault create vault
ansible-vault encrypt_string --vault-id vault '<VALUE TO ENCRYPT>' --name '<VAR NAME>'
```

## execute playbook with default inventory

```
ansible-playbook playbook.yml --vault-password-file vault
```

## running playbook with an inventory file
```
ansible-playbook -i <inventory file name>  playbook.yml --vault-password-file vault
```

