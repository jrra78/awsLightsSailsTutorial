# Linux Server Setup
Basic tutorial for building and deploying applications in AWS LightSails VPS With Ubuntu Linux

## Security: setting the firewall
UFW (Uncomplicated Fire Wall( is installed but disabled on some linux distributions (i.e. Ubuntu), and you need to enable it before opening any ports on your server. But if anything, you can manually install UFW by running the following command: 
To install UFW use: 
```
$ sudo apt install -y ufw
```
### Ports configuration
The basic UFW configuration will require access to the following: 

| port | usage |
|------|----------|
| 22   | ssh  |
| 80   | http |
| 443  | https |
| 3306 | mysql |

Access can be granted by the following command
```
sudo ufw allow <port>/<protocol>
```
To acchieve the basic configuration, the following commands can be used:
```
$ sudo ufw allow 22
$ sudo ufw allow 80
$ sudo ufw allow 443
$ sudo ufw allow 3306
```

### Check UFW Status

To verify what is currently blocked or allowed, you may use the verbose parameter when running ufw status, as follows:
```
$ sudo ufw status

```
### Enable UFW
To enable UFW on your server, run:
```
$ sudo ufw enable
```
Alternatively
```
$ sudo ufw --force enable
```
### Disable UFW
To disable UFW on the server, use the following command:
```
$ sudo ufw disable
```
