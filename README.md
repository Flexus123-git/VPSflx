# VPSflx
# Deploying a Personal VPN on a VPS using Xray (VLESS + Reality)

This is a step by step guide for setting up a VPN server on a VPS using Xray (VLESS + Reality).

This setup can be useful in countrys where most popular VPN protocols blocked.

⚠ This guide doesn't advertise any VPS platforms.

---

## 📋 Requirements

### 1️⃣ Rent a VPS

To deploy your VPN server, you need to rent VPS(Virtual Private Server)

Popular VPS providers:

- DigitalOcean
- Hip-hosting
- Timeweb

### VPS Requirements

- A VPS with **2 GB RAM** is ehough for a personal VPN server.
- Choose **Ubuntu 24.04 LTS** or higher as your VPS server system.
- After renting the server, you will get:
  - Server IP address (e.g., 139.213.12.21)
  - Login (usually `root`)
  - Password

---

## 🖥 Step 2 — Connecting to the Server via SSH

To manage your VPS, you need an SSH client

You can use the standart terminal on Windows or macOS, but a third-party SSH client is more available

I recommend using Termius (free for non-commercial use)

### Connecting with Termius

1. Click **"New Host"**
2. Enter your server IP address from your VPS server dashboard
3. Enter your username from dashboard
4. Enter your password from dashboard
5. default SSH port - **22**

Then click **Connect**.

---

## ⚙ Step 3 — System Update and 3x-ui Installation

### 1️⃣ Update the System

Before installing the panel, you should to update the system packages:

```bash
sudo apt-get update -y
sudo apt-get upgrade -y
```

These commands:
	•	Check for available package updates
	•	Upgrade installed packages to the latest versions

### 2 3x-ui installation


To install the 3x-ui dashboard, run the official installation script by MHSanaei:

`bash <(curl -Ls https://raw.githubusercontent.com/mhsanaei/3x-ui/master/install.sh)`

During installation, you will see this question:

**Would you like to customize the Panel Port settings?**
Answer:**n** for easy installation (Default settings are convenient for most of users)

After the installation completes, the script will generate panel informations:
For example: Username: <generated_username>
             Password: <generated_password>
             Port: 40608
             WebBasePath: <generated_path>
			 URL: https://ip:port/webpath
	
			





