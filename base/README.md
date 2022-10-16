Base role
=========

Apply firewall rules. Config sftp. Install and config webserver.

Role Variables
--------------

```yml
# SSH
SSH_PORT: 22  # Set ssh port for firewall

# SFTP
SHARE_DISK_GROUP: sharedisk  # Group name for sftp access to ext drive
SHARE_DISK_USER: jdshare  # User name for sftp access to an ext drive
SHARE_PUBLIC_USER: shareuser  # User name for sftp access to public dir on ext drive
DISK_LABEL: disk  # Exd drive label

# NGINX
SSL_CERT_NAME: cert.crt # SSL Cert name
SSL_KEY_NAME: cert.key # SSL Key name
DH_NAME: dhparam.pem # DH group name
SSL_CERT_PATH: ./assets/{{ SSL_CERT_NAME }} # SSL Cert path
SSL_KEY_PATH: ./assets/{{ SSL_KEY_NAME }} # SSL Key path
DH_PATH: ./assets/{{ DH_NAME }} # DH group path

```

Example Playbook
----------------

```yml
  - hosts: servers
    roles:
       - role: base
```

License
-------

GPL

Author Information
------------------

[Grell Gragham](https://github.com/ggragham)