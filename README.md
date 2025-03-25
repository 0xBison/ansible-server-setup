Simple setup script for server with ansible

## Usage

Create inventory.ini file. If you're using ssh:

```ini
[webserver]
your_server_ip ansible_user=user ansible_ssh_private_key_file=~/.ssh/id_rsa
```

```ini
[webserver]
your_server_ip ansible_user=user
```

and run

`ansible-playbook -i inventory.ini setup.yml --ask-pass` (--askpass needed if using password auth)