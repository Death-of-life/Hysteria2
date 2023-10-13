# Hysteria2
Hysteria 2 One-Click Installation Script

## User Manual
### 1. Resolve the domain name to your VPS IP
**If you are using Cloudflare, do not turn on the CDN service.**

### 2. Ensure that port 80 of the VPS is not occupied
This script uses ACME to automatically apply for certificates, so please make sure that port 80 is available. You can use the following command to determine: 
```bash
lsof -i :80
```

### 3. Execute installation command.
```bash
bash <(curl -Ls https://qwq.mx/hy2)
# or
bash <(curl -Ls https://github.com/missuo/Hysteria2/raw/main/hy2.sh)
```


### 4. Enter the configuration information according to the prompts.
```
Enter the port (default: 8443): 
Enter the domain: 
Enter the password (default: Hy2Best2024@):
```

### Uninstall
```bash
bash <(curl -fsSL https://get.hy2.sh/) --remove
rm -rf /etc/hysteria
userdel -r hysteria
rm -f /etc/systemd/system/multi-user.target.wants/hysteria-server.service
rm -f /etc/systemd/system/multi-user.target.wants/hysteria-server@*.service
systemctl daemon-reload
```

## Client
### Surge
```
🇺🇸 NodeName = hysteria2, us.example.com, 8443, password=Hy2Best2024@, sni=us.example.com, download-bandwidth=600
```
### Shadowrocket
Manually fill in according to the information you entered.

## Author
**Hysteria2** © [Vincent Young](https://github.com/missuo), Released under the [MIT](./LICENSE) License.<br>
