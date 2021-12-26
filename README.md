# Linux Server Setup
Basic tutorial for building and deploying applications in AWS LightSails VPS With Ubuntu Linux

## Security: setting the firewall
UFW (Uncomplicated Fire Wall( is installed but disabled on some linux distributions (i.e. Ubuntu), and you need to enable it before opening any ports on your server. But if anything, you can manually install UFW by running the following command:

```
$ sudo apt install -y ufw
```

```
sudo ufw allow <port>/<protocol>
```

| port | protocol |
|------|----------|



```
$ sudo ufw allow ssh
$ sudo ufw allow http
$ sudo ufw allow 443/tcp
$ sudo ufw --force enable
$ sudo ufw status
```

### Check UFW Status

Now that you have enabled UFW and set some rules, check the current firewall table and operation.

```
$ sudo ufw status

```
