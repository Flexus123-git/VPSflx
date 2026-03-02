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

# ⚙️ Step 3 — System Update and 3x-ui Installation

## 1️⃣ Update the System

Before installing the panel, update your system packages:

```bash
sudo apt-get update -y
sudo apt-get upgrade -y
```

### 🔎 What These Commands Do

- `apt-get update` — checks for available package updates  
- `apt-get upgrade` — upgrades installed packages to the latest versions  

Keeping your system updated helps prevent compatibility and security issues.

---

## 2️⃣ Install 3x-ui

To install the **3x-ui** dashboard, run the official installation script by **MHSanaei**:

```bash
bash <(curl -Ls https://raw.githubusercontent.com/mhsanaei/3x-ui/master/install.sh)
```

---

### ❓ Installation Prompt

During installation, you will see:

```
Would you like to customize the Panel Port settings?
```

For a quick and easy setup, type:

```bash
n
```

(Default settings are suitable for most users.)

---

## 🔐 After Installation

Once installation is complete, the script will generate your panel credentials.

Example output:

```
Username: <generated_username>
Password: <generated_password>
Port: 40608
WebBasePath: <generated_path>
URL: https://ip:port/webpath
```

⚠️ **Important:** Save this information securely — you will need it to access the panel.
	
			





