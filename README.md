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

# ⚙️ Step 3 — System Update and 3x-ui Installation:

## 1️⃣ Update the System

Before installing the 3x-ui dashboard, you should update your system packages:

```bash
sudo apt-get update -y
sudo apt-get upgrade -y
```

### 🔎 These commands:

checks for available package updates and upgrades installed packages to the latest versions  

---

## 2️⃣ Install 3x-ui

To install the **3x-ui** dashboard, copy in terminal the official installation script by MHSanaei:

```bash
bash <(curl -Ls https://raw.githubusercontent.com/mhsanaei/3x-ui/master/install.sh)
```

During installation, you will see:

```
Would you like to customize the Panel Port settings?
```

For a quick and convenient setup, type:

```bash
n
```

---

## 🔐 After Installation

After installation, you will receive data from the panel

Example:

```
Username: <randeom_username>
Password: <random_password>
Port: 45434
WebBasePath: <random_path>
URL: https://ip:port/webpath
```

⚠️ **Important:** Save this information — you need it to get access the panel.

## 🚀 Step 4: Inbound Creation

After installing **3x-ui**, you need to create an inbound for connection.

First step, copy the URL you got after installation and paste it into any browser.  
Log in using your **username** and **password**.

After you are inside the panel, go to:

**Inbound → Add Inbound**

Fill in the fields this information:

- **Remark:** (Any name you like)  
- **Listen IP:** Your server IP  
- **Port:** `443`  
- **Security:** `Reality`  
- **Client Flow:** `xtls-rprx-vision-udp443`  
- **Target / SNI:** Any website that is **not blocked in your country**

Then:

1. Click **Get New Cert**
2. Click **Create**

✅ Your inbound is now created.

---

## 📱 Client Applications

You can connest by qr or Export All URLs from your inbound.
You can connect using this apps:

### Android / iOS
- **V2Ray**
- **Hiddify**

### macOS
- **V2Ray** (recommended)

### Windows
- **NekoBox**
---

## 🔐 Security Tips

- Always use port `443`
- Choose a popular and trusted domain for SNI
- Keep your panel credentials private
- Disable unused inbounds
- Regularly update your 3x-ui panel
  
---

Your server is now ready to use 🚀

	
			





