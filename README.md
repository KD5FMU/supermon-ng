# supermon-ng

**supermon-ng** is a modernized and extensible version of the original Supermon dashboard for managing and monitoring Asterisk-based systems such as AllStarLink nodes. It offers a streamlined web interface and compatibility with today's system environments.

## Features

- Responsive and mobile-friendly web UI
- Enhanced security and codebase modernization
- Simple installer script for quick deployment
- Easily customizable and extendable
- Compatible with Debian-based systems

## Quick Install

First, ensure `rsync` and other necessary tools are installed:

```bash
sudo apt update && sudo apt install -y rsync
```

Then, download and run the installer script:

```bash
wget -q -O supermon-ng-installer.sh "https://raw.githubusercontent.com/hardenedpenguin/supermon-ng/refs/heads/main/supermon-ng-installer.sh"
chmod +x supermon-ng-installer.sh
sudo ./supermon-ng-installer.sh
```

> ⚠️ **Note:** This installer is designed for Debian-based systems (e.g., Debian, Ubuntu, or AllStarLink distributions). Run as root or with `sudo`.

## Post-Installation

After the installer completes and you have configured an initial user, it is recommended to review and customize user permissions.

You can do this by editing the `authuser.inc` file, which is typically located in your web server's directory for supermon-ng (e.g., `/var/www/html/supermon-ng/`).
Choose the option that works best for you, the sed statement is best if you are the sole admin or the lead admin.
```bash
sudo nano /var/www/html/supermon-ng/user_files/authuser.inc
```
```bash
sudo sed -i 's/admin/username/g' /var/www/html/supermon-ng/user_files/authuser.inc
```
If you are using the sed method, please ensure you replace username with the username you have created for your supermon-ng login.

## Requirements

- Debian-based Linux system
- Apache2 or other compatible web server
- Asterisk with AllStarLink node configured
- PHP 7.4 or later
- Rsync

## Contributions

Contributions, issues, and feature requests are welcome! Please fork the repository and submit a pull request.

## License

[MIT](LICENSE)

👉 If you want to help Jory out with his efforts on making things better for all of us then please consider makeing a donation to his efforts.🇺🇸
---
<a href="https://www.paypal.com/donate?token=IyATJ7p91vnH0tLglypNy2DxIZ3G2VmpWddIzltxRzY4kpcF0hPRHPj7F9ipe3YvfujL-1een4QH5Te5" target="_blank">
  <img src="https://img.shields.io/badge/Donate%20with-PayPal-00457C?style=for-the-badge&logo=paypal&logoColor=white" />
</a>

<a href="https://cash.app/$anarchpeng" target="_blank">
  <img src="https://img.shields.io/badge/Donate-CashApp-00C244?style=for-the-badge&logo=cashapp&logoColor=white" />
</a>

<!-- Zelle uses email/phone inside your bank app; no public pay URL exists. -->
<a href="mailto:geekypenguin@gmail.com?subject=Zelle%20Donation%20for%20Jory%20Pratt%20-%20W5GLE&body=I%27d%20like%20to%20send%20a%20Zelle%20donation.">
  <img src="https://img.shields.io/badge/Donate%20via-Zelle-6D1E72?style=for-the-badge&logo=zelle&logoColor=white" />
</a>

**Send via Zelle to:** `geekypenguin@gmail.com` (Jory Pratt – W5GLE)
