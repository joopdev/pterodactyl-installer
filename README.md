# 🦅 Pterodactyl Ultimate All-in-One Installer

A powerful, secure, and user-friendly bash script designed to automate the installation, management, and updating of the Pterodactyl Panel and Wings. Whether you are a beginner or a pro, this toolkit handles the heavy lifting for you.

## 🚀 Quick Install

Run the following command on your server (Ubuntu/Debian) to launch the interactive toolkit:

```bash
bash <(curl -s https://gist.githubusercontent.com/joopdev/bf1903613be02cee1681cefb2459b43d/raw)
```

---

## ✨ Features
* **Panel Installation:** Automated setup of PHP 8.3, MariaDB, Nginx, and Redis.
* **Wings (Node) Setup:** Automatic Docker installation and Wings configuration.
* **All-in-One Option:** Install both Panel and Wings on the same machine.
* **Smart Updates:** Easy one-click updates for both Panel and Wings.
* **SSL Support:** Automated Let's Encrypt certificates via Certbot.
* **Global-Ready:** Automatic timezone detection with manual override.
* **High Security:** Double-confirmation uninstaller and secure password generation.

---

## 📋 Prerequisites
Before running the script, ensure you have:
1.  **A Clean Server:** Ubuntu 22.04, 24.04, or Debian 11/12.
2.  **A Domain Name:** An A-Record (e.g., `panel.yourdomain.com`) pointing to your server IP.
3.  **Root Access:** You must run the script as `root`.

---

## 🛠 What to Expect (The Process)
When you run the script, it will guide you through several questions:
1.  **FQDN:** The domain name you set up (e.g., `panel.example.com`).
2.  **Email:** Used for the SSL certificate and the initial admin account info.
3.  **Database Password:** You can provide one or let the script generate a strong one for you.
4.  **Timezone:** It will suggest your server's current timezone, but you can enter any valid PHP timezone.
5.  **Version:** Choose between the `Latest Stable` release or a `Specific/Beta` version.

---

## ⚠️ Uninstallation
We include a "Danger Zone" option. To prevent accidental data loss, removing the Panel or Wings requires a two-step verification:
1.  Type `YES` to proceed.
2.  Type `DELETE` to confirm permanent removal.

---

## 🧑‍💻 Credits & Contact
Created with ❤️ by **JoopDev**.

* **Developer:** JoopDev
* **Email:** [info@joopdev.com](mailto:info@joopdev.com)
* **Support:** Open an issue on this repository for bugs or feature requests.

---
*Disclaimer: This script is not an official Pterodactyl project. Use it at your own risk.*
---
