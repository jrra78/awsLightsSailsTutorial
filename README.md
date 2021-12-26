# Linux Server Setup
Basic tutorial for building and deploying applications in AWS LightSails VPS With Ubuntu Linux

## Security: setting the firewall
UFW (Uncomplicated Fire Wall( is installed but disabled on some linux distributions (i.e. Ubuntu), and you need to enable it before opening any ports on your server. But if anything, you can manually install UFW by running the following command:

```
$ sudo apt install -y ufw
```
