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
port 22 (ssh), 80 (http) and 443 (https)

| port | protocol |
|------|----------|
| 22   | ssh  |
| 80   | http |
| 443  | http |
| 3306 |

$ sudo ufw allow 22/tcp
$ sudo ufw allow 80/tcp comment 'accept Apache'
$ sudo ufw allow 443/tcp 'accept HTTPS connections'
$ sudo ufw allow 3306 'accept HTTPS connections'

```
$ sudo ufw allow ssh
$ sudo ufw allow http
$ sudo ufw allow 443/tcp
$ sudo ufw --force enable
$ sudo ufw status
```

### Check UFW Status

To verify what is currently blocked or allowed, you may use the verbose parameter when running ufw status, as follows:
```
$ sudo ufw status

```
### Enable UFW
To enable UFW on your server, run:
```
sudo ufw enable
```
### Disable UFW
To disable UFW on the server, use the following command:
```
$ sudo ufw disable
```
