# T-RMM-Baremetal-HAProxy

T-RMM config for HAProxy on bare metal.

Assumes fresh install of HAProxy before any configuartion

Ubuntu config file location: /etc/haproxy/haproxy.cfg

Create symlinks for certs to simplify process and server configs:
```text
sudo ln -s /etc/letsencrypt/live/(domain)/fullchain.pem /etc/ssl/certs/fullchain.pem
sudo ln -s /etc/letsencrypt/live/(domain)/privkey.pem /etc/ssl/private/privkey.pem
```

Make sure to create DH pem:
```text
sudo openssl dhparam -out /etc/ssl/certs/dhparam.pem 4096
```
