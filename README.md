<div align="center">

# 🔐 Cybersecurity - How to setup HexStrike MCP Server & JTR Password Cracking AI-version (EXTRA)

**W3-Extra- M1: How to setup HexStrike MCP Server & W3-Extra-M2: JTR Password Cracking AI-version**
</div>

<p align="center">
  <img src="https://img.shields.io/badge/Skill-Cybersecurity-404040?style=flat-square&labelColor=C00000" />
  <img src="https://img.shields.io/badge/Ver-Virtualbox%20v7.2.22-0070C0?style=flat-square&labelColor=000000" />
  <img src="https://img.shields.io/badge/Kali%20Linux-v2026.3-E87500?style=flat-square&labelColor=000000&logo=kalilinux&logoColor=white" />  
  <img src="https://img.shields.io/badge/Claude%20Desktop-E87500?style=flat-square&labelColor=000000&logo=Claude&logoColor=white" />
  <img src="https://img.shields.io/badge/HexStrike%20AI-C00000?style=flat-square&labelColor=000000&logo=foobar2000&logoColor=white" />
  <img src="https://img.shields.io/badge/MCP%20Server-HexStrike%20AI-238F89?style=flat-square&labelColor=000000" />
  <img src="https://img.shields.io/badge/MCP%20Client-Claude%20Desktop-238F89?style=flat-square&labelColor=000000" />
  <img src="https://img.shields.io/badge/Ver-John%20The%20Ripper%20v1.9-0070C0?style=flat-square&labelColor=000000" />
  <img src="https://img.shields.io/badge/Security%20Auditing-C00000?style=flat-square&labelColor=000000&logo=kalilinux&logoColor=white" />
  <img src="https://img.shields.io/badge/Skill-AI%20Automated%20Cybersecurity-404040?style=flat-square&labelColor=C00000" />
  <img src="https://img.shields.io/badge/Skill-Agentic%20AI-404040?style=flat-square&labelColor=C00000" />
  <img src="https://img.shields.io/badge/Skill-Prompt%20Engineering-404040?style=flat-square&labelColor=C00000" />
  <img src="https://img.shields.io/badge/Skill-MCP%20Orchestration-404040?style=flat-square&labelColor=C00000" />  
  <img src="https://img.shields.io/badge/Skill-Password%20Hacking-404040?style=flat-square&labelColor=C00000" />
  <img src="https://img.shields.io/badge/Skill-Dictionary%20Attacks-404040?style=flat-square&labelColor=C00000" />
  <img src="https://img.shields.io/badge/Skill-Catch%20The%20Flag-404040?style=flat-square&labelColor=C00000" />
  <img src="https://img.shields.io/badge/Skill-Hash%20Cracking-404040?style=flat-square&labelColor=C00000" />
  <img src="https://img.shields.io/badge/Skill-Data%20Security%20&%20Privacy-404040?style=flat-square&labelColor=C00000" />
  <img src="https://img.shields.io/badge/Ethical%20Hacking-E87500?style=flat-square&labelColor=000000&logo=kalilinux&logoColor=white" />
  <img src="https://img.shields.io/badge/Penetration%20Testing-C00000?style=flat-square&labelColor=000000&logo=kalilinux&logoColor=white" />
  <img src="https://img.shields.io/badge/GitHub-404040?style=flat-square&labelColor=0070C0&logo=github&logoColor=white" />
  <img src="https://img.shields.io/badge/NetworkWalks-404040?style=flat-square&labelColor=C00000" />
  <img src="https://img.shields.io/badge/AZIAGBEDO%20KOKOU%20SODJINE%20-%20CCEP-C00000?style=flat-square" />
</p>

---

<p align="center">
  <img src="/images/hexstrike.jpg" width="400" height="175" alt="HexStrike AI">
</p>

---

## 📌 Project Overview

This project focuses on password cracking using AI, MCP Server and MCP client in a lab-environment. It helps develop Cybersecurity skills such as Ethical Hacking, Penetration Testing and specially AI automated cybersecurity. It is composed of two modules : Module 1 (M1) and Module 2 (M2). 

The purpose of M1 is to setup a HexStrike MCP Server with Claude Desktop as a MCP client. The M2 aims to use JTR via MCP orchestration for password cracking.

The password-cracking activities presented in this project should only target authorized files and devices or those you own for security testing.

---

## ⚙️ The lab configuration

| 🧩 Component       | ⚙️ Configuration   |
| ------------------ | ------------------  |
| 🖥️ Host OS         | Windows 11         |
| 🧠 Host RAM        | 16 GB              |
| ⚡ Processor       | Intel Core i5      |
| 🧰 Hypervisor      | VirtualBox 7.2.22  |
| 🐉 Security OS     | Kali Linux 2026.3  |
| 🧠 Kali RAM        | 4096 MB            |
| 🌐 Virtual Network | NAT Network        |
| 📡 Network Address | 10.0.0.0/24        |
| 🐧 Kali IP Address | 10.0.0.2/24        |
| 🚪 Default Gateway | 10.0.0.1           |
| 🌍 DNS Server      | 8.8.8.8            |
| 🔮 Future VM Range | 10.0.0.3–10.0.0.99 |

---

# 🔓 M1 - Setting up a HexStrike MCP Server

---

## ⚓ Background

To experiment AI automated cybersecurity, we are setting up a Hexstrike MCP Server with Claude desktop on Kali Linux in a lab-environment. The HexStrike MCP server integrates almost 150 Cybersecurity tools, including the popular password cracking tool John the Ripper (JTR) that is used by security professionals to test how strong passwords are. 

---

## 🎯 Objective

The PM1's objective is to set up a Hexstrike MCP Server with Claude desktop as client on a Kali Linux VM.

---

## Installation of Claude Desktop

We downloaded and installed Claude Desktop using the Github repository mentionned in the [**Tools & Resources**](#-tools--resources) section.

---

### Adding the GPG key

We used the following command to add the gpg key :

````bash
curl -fsSL https://pkg.claude-desktop-debian.dev/KEY.gpg | sudo gpg --dearmor -o /usr/share/keyrings/claude-desktop.gpg
````

---

![screenshot_1.png](/images/screenshot_1.png)

---

### Adding the repository

````bash
echo "deb [signed-by=/usr/share/keyrings/claude-desktop.gpg arch=amd64,arm64] https://pkg.claude-desktop-debian.dev stable main" | sudo tee /etc/apt/sources.list.d/claude-desktop.list
````

---

### Updating and installing

````bash
sudo apt update && sudo apt install claude-desktop
````

---

![screenshot_2.png](/images/screenshot_2.png)

---

We installed Claude Desktop and signed in.

---

![screenshot_3.png](/images/screenshot_3.png)

---

## Downloading HexStrike MCP

We downloaded HexStrike MCP using the Github repository mentionned in the [**Tools & Resources**](#-tools--resources) section.

### Cloning the repository

Command used :

````bash
git clone https://github.com/0x4m4/hexstrike-ai.git
````

---

![screenshot_4.png](/images/screenshot_4.png)

---

We moved into the hexstrike-ai directory.

````bash
cd hexstrike-ai
````

---

### Creating virtual environment

We created a virtual environment on the Kali VM.

````bash
python3 -m venv hexstrike-env
````

We activated the environment :

````bash
source hexstrike-env/bin/activate # Linux/Mac
````

To activate the environment on a Windows PC:

````bash
hexstrike-env\Scripts\activate
````

---

### Installing Python dependencies

We used the following command to install the requirements.

````bash
pip3 install -r requirements.txt
````

We remarked that pip was backtracking the versions of **angr** for a long time because of compatibility issues. It was trying all its 216 versions satisfying the line **"angr>=9.2.0,<10.0.0"** in the requirements.txt.

We opened the requirements.txt and found out that **angr** was not mandatory for the use of HexStrike MCP in our project. It is **"CONDITIONALY USED"** for **"BINARY ANALYSIS"**.

We commented that line about **angr**, saved the requirements.txt new version and installed successfully the requirements.

---

![screenshot_5.png](/images/screenshot_5.png)

---

![screenshot_6.png](/images/screenshot_6.png)

---

We checked the installation status with these commands:

````bash
pip check
````

and

````bash
python -c "import flask, requests, psutil, aiohttp, bs4, selenium, mitmproxy, pwn; print('OK')"
````

---

![screenshot_7.png](/images/screenshot_7.png)

---

To launch the MCP Server, we used the following commands:

````bash
cd ~/hexstrike-ai
````

````bash
source hexstrike-env/bin/activate
````

````bash
python3 hexstrike_server.py
````

---

![screenshot_8.png](/images/screenshot_8.png)

---

### Editing MCP Server configuration on claude desktop

We opened Claude Desktop. We went to **`Settings > Desktop app > Extensions`** and then clicked on **`Edit config`** under **`Local MCP servers`**.

---

![screenshot_9.png](/images/screenshot_9.png)

---

We found out the name of the configuration file.

---

![screenshot_10.png](/images/screenshot_10.png)

---

We right-clicked on the configuration file and opened its path in a terminal. 

We edited the file with :

````bash
sudo nano claude_desktop_config.json
````

---

![screenshot_11.png](/images/screenshot_11.png)

---

![screenshot_12.png](/images/screenshot_12.png)

---

Claude Desktop showed then that the MCP server was running.

---

![screenshot_13.png](/images/screenshot_13.png)

--- 

We tested the setup with this prompt in the chat of Claude Desktop :

````text
please check the health of the HexStrike MCP server and present results with a small dashboard
````

![screenshot_14.png](/images/screenshot_14.png)

---

![screenshot_15.png](/images/screenshot_15.png)

---

![screenshot_16.png](/images/screenshot_16.png)

---

We also opened the MCP server health page in a browser at the address :

````text
http://localhost:8888/health
````

---

![screenshot_17.png](/images/screenshot_17.png)

---

We wisely took a snapchat of the Kali VM to save its state in Virtualbox.

---

![screenshot_18.png](/images/screenshot_18.png)

---

# 🔓 M2 - JTR Password Cracking AI-version

---

## ⚓ Background

We are cracking the password of the PDF file "My Locked PDF1.pdf" using JTR JOHN with the help of AI (Hexstrike-AI MCP with Claude desktop in Kali Linux).

This module helps understand and experiment AI automated cybersecurity. It also helps understand how password cracking works step by step and why strong passwords are important for protection.

Related Info:

- Lab environment: Hexstrike-AI MCP server with Claude desktop on Kali Linux VM (follow the attached Hexstrike-AI MCP server setup guide)

- The target file "My Locked PDF1.pdf" is in the folder "/encrypted file/".

---

## 🎯 Objective

The M2's objective is to crack the password of "My Locked PDF1.pdf" using JTR JOHN with the help of AI (Hexstrike-AI MCP with Claude desktop in Kali Linux).

---

## 👣 Step 1

We copied the encrypted PDF file **`My Locked PDF1.pdf`** to our Kali VM desktop. 

The said PDF is from the Networkwalks project's Google Drive link. The downloaded file is available in **`/encrypted file/`**

---

![screenshot_19.png](/images/screenshot_19.png)

---

## 👣 Step 2

We opened Claude AI desktop on our Kali Linux.

And we entered the prompts below: 

````text
Check if John the Ripper is installed in this Hexstrike MCP and show me its version
````

---

![screenshot_20.png](/images/screenshot_20.png)

---

````text
Please calculate the hash value of this PDF file: /home/kali/Desktop/My Locked PDF1.pdf
````

---

![screenshot_21.png](/images/screenshot_21.png)

---

````text
Please use JTR tool in this Hexstrike MCP server to crack the password of this PDF file. Use the rockyou.txt wordlist dictionary.
````

---

![screenshot_22.png](/images/screenshot_22.png)

---

We screenshot the logs of the MCP server while cracking the password.

---

![screenshot_23.png](/images/screenshot_23.png)

---

We checked the successful completion of the password cracing with the command :

````bash
john --show --format=PDF /tmp/pdf.hash
````

---

![screenshot_24.png](/images/screenshot_24.png)

---

The password had been cracked by AI.

We copied the shown password and we opened the locked PDF file. 

---

![screenshot_25.png](/images/screenshot_25.png)

---

We entered the cracked password **`good-luck`**.

---

![screenshot_26.png](/images/screenshot_26.png)

---

We validated the entered password and the locked PDF file opened successfully.

---

![screenshot_27.png](/images/screenshot_27.png)

---

### Captured Flag

The captured flag is **`nw{cybersecurity_flag_captured_2608}`**.

---

![1_falg1.png](/images/1_falg1.png)

---

## Project Short Video

We recorded a short video of the project completion.

https://github.com/user-attachments/assets/61498543-e3fa-4762-a4cc-ce149b9cbfc8

---

# 💡 What I practiced

Through this project, I practiced password hacking with AI. I set up a HexStrike MCP server and Claude Desktop as MCP client. I used the setup to get the hash value and found the password to open a locked pdf file. I experimeted and practiced AI automated cybersecurity. I orchestrated hacking tasks with the HexStrike MCP server and the client Claude Desktop. The abilities developed in these activities can be used to hack many other kinds of passwords, including credentials and wi-fi passwords. I tested the data security regarding their confidentiality. I captured the hidden flags. I used the popular Cybersecurity tool John The Ripper (JTR) via a MCP server. I experienced Agentic AI. I also demonstrated Prompt Engineering skills.

I demonstrated AI Automated Cybersecurity, Ethical Hacking and Data Security skills.

The most important skills I demonstrated include:

### 1. AI Automated Cybersecurity

I set up a HexStrike MCP server and Claude Desktop as MCP client. I used the setup for hacking.

### 2. Catch The Flag

I captured the hidden flags and documented them faithfully.

### 3. Password hacking

I used JTR and Networkwalks tools to hack the passwords and capture the flags. 

### 4. Data Security

I used AI and JTR tools to perform password auditing for Data security.

### 5. Prompt Engineering

I wrote prompts to assign tasks to Claude Desktop as a MCP client for the HexStrike MCP server. The prompts brought to the expected results successsfully.

### 6. Cyber Threat Intelligence 

By testing the strength of the passwords and the data security earlier, I demonstrated Cyber Threat Intelligence skills, including Threat Hunting and Threat Detection.

### 7. Intrusion Prevention (IPS)

By testing the strength of the passwords for data security and early detecting their weakness and related threats, I can enhance the security level and prevent an attacker from hacking the passwords. The PDF files might contain critical data like credentials, server details that could help an attacker to perform an intrusion.

### 8. Security-tool experimentation

Using different tools such as JTR John, HexStrike-AI MCP server, as well as Claude Desktop AI MCP client to hack passwords is a practical way to experiment and master security tools.

### 9. Security mindset

A security mindset in cybersecurity is a proactive, analytical way of thinking. I demonstrated that mindset throughout this project by using appropriate AI tools and testing the strength of the passwords that were supposed to ensure data privacy.

### 10. Documentation

I documented tools, platforms links, screenshots, tasks and solutions. That is an important part of a professional cybersecurity project.

---

# 🔐 Security & Ethical Use

This project is intended strictly for education purposes only.

>>⚠️ Important: The skills demonstrated in this project must only be used on systems that you own or have explicit permission to test. Do not use the knowledge or the tools to attack unauthorized systems.

---

# 🔗 Tools & Resources

- **Claude Desktop download:** [https://github.com/aaddrick/claude-desktop-debian](https://github.com/aaddrick/claude-desktop-debian)]
- **Hexstrike MCP download:** [https://github.com/0x4m4/hexstrike-ai](https://github.com/0x4m4/hexstrike-ai)

---

# 👤 Author

**AZIAGBEDO KOKOU SODJINE**\
Cybersecurity Professional B084

LinkedIn: https://www.linkedin.com/in/kokou-sodjin%C3%A8-aziagbedo-434b2949

---

## 📌 Project Information

**Program Name:** Cybersecurity at Networkwalks | **Week:** 03 | **Project:** How to setup HexStrike MCP Server & JTR Password Cracking AI-version (EXTRA)| **Repository:** GitHub

