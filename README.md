# Raspberry Pi Ethical Hacking Web Server

This project sets up a realistic web server on a Raspberry Pi 4B to simulate a real-world environment for learning ethical hacking, web security, and system administration.

## 🔧 Features

- Apache web server with PHP support
- MariaDB (MySQL) database integration
- Supports HTML, CSS, JavaScript, and PHP
- Can host realistic sites for XSS, SQLi, and other local testing
- Custom virtual host setup
- Local and network access via `http://<raspberrypi_ip>`

## 🛠️ Requirements

- Raspberry Pi 4B (or similar)
- Raspberry Pi OS (Debian-based)
- Internet connection
- Git (for pushing to GitHub)
- Optional: PHP, MariaDB, Python/Flask

## 🚀 Installation

```bash
sudo apt update && sudo apt upgrade -y
sudo apt install apache2 php libapache2-mod-php mariadb-server php-mysql git -y
```
Set up project directory:
```bash
sudo nano /etc/apache2/sites-available/myproject.conf
```
Create virtual host file:
```bash
sudo nano /etc/apache2/sites-available/myproject.conf
```
Paste and enable:
```bash
<VirtualHost *:80>
    DocumentRoot /var/www/myproject
</VirtualHost>
```
```bash
sudo a2ensite myproject.conf
sudo a2dissite 000-default.conf
sudo systemctl reload apache2
```
🌐 Access Your Site
Open a browser and go to:
```bash
http://<your_raspberry_pi_ip>
```
🧪 Use Cases
Host dummy login pages (educational use)

Practice XSS, SQLi, file upload tests

Build & test local WordPress or PHP sites

Network scanning and web app testing in lab

⚠️ Legal Disclaimer
This project is for educational and ethical purposes only. Never use these techniques on any system without proper authorization.

📦 License
MIT License – Free to use, modify, and share with proper credit.

---

Let me know if you'd like a GitHub-ready version with badges or a license file added too!
