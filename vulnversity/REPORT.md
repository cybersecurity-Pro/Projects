# 🔓 TryHackMe Lab Walkthrough – Vulnversity  

## 📌 Introduction  
This project is part of the **Offensive Pentesting Path** on [TryHackMe](https://tryhackme.com).  
The lab we are working on is **Vulnversity**, a beginner-friendly CTF room focused on web vulnerabilities, privilege escalation, and enumeration.  

For this walkthrough, I am using **Kali Linux on VirtualBox**.  
- Connection to the TryHackMe network is done via **OpenVPN**.  
- Alternatively, you can use the **AttackBox** (browser-based Kali provided by THM), which is already connected to the lab environment.  

---

## 🚀 Step 1: Deploying the Target Machine  
The first step is to deploy the vulnerable machine provided by TryHackMe.  

- Start the machine from the THM portal.  
- Wait **1 minute** for the target IP to appear.  
- Allow **4–5 minutes** for the machine to fully boot.  

📷 **Screenshot:**  
![Deploying the Machine](./screenshots/deploy-machine.png)  ---

## 🔎 Step 2: Enumeration with Nmap  
After the target machine was up, I conducted an **Nmap scan** to identify open ports and running services.  
I used the `-A` flag since it provides OS detection, service versions, and script scanning in one command.  

```bash
sudo nmap -A 10.10.68.23
```
📷 Screenshot:


Results from the scan:

Port 21/tcp → FTP (vsftpd 3.0.3)

Port 22/tcp → SSH (OpenSSH 7.2p2)

Port 139, 445/tcp → SMB service running

Port 3128/tcp → Squid HTTP proxy

Port 3333/tcp → Apache web server (Vuln University)

👉 The web server on port 3333 stands out as a potential entry point for exploitation.

