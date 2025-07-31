# Install Nessus Essentials

## 1. Download Nessus Essentials
- Go to [https://www.tenable.com/products/nessus/nessus-essentials](https://www.tenable.com/products/nessus/nessus-essentials)

## 2. Install on Ubuntu Server
```bash
sudo dpkg -i Nessus-<version>.deb
sudo systemctl start nessusd.service
```
## 3. Access Web Interface
- Open: https://<server-ip>:8834
- Enter the activation code
- Create an admin account
