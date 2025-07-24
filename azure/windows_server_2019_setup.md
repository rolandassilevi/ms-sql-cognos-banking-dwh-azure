# 🧱 Windows Server 2019 Setup Guide for Cognos + SQL + IIS

This guide outlines the steps to configure a Windows Server 2019 VM on Azure to host Microsoft SQL Server, IBM Cognos Analytics, and IIS.

---

## 🖥️ 1. VM Creation on Azure

- VM Size: Standard_D2s_v3
- OS: Windows Server 2019 Datacenter
- Disk: 128 GB Premium SSD
- Inbound ports: 3389 (RDP), 80 (HTTP), 443 (HTTPS), 1433 (SQL)

---

## ⚙️ 2. Post-Deployment Server Configuration

### 🔹 System Updates
- Install all available Windows Updates
- Enable `.NET Framework 4.7+`

### 🔹 Remote Desktop
- Ensure RDP is enabled (System > Remote settings)

---

## 🌐 3. IIS Setup

### Add Server Role:
- Open **Server Manager** > Add Roles and Features
- Add role: **Web Server (IIS)**
- Include features:
  - Web Server > Common HTTP Features
    - Static Content
    - Default Document
    - Directory Browsing
  - Application Development
    - .NET Extensibility 4.7
    - ASP.NET 4.7
  - Management Tools
    - IIS Management Console

### Test:
- Open browser → http://localhost → confirm IIS welcome page

---

## 💽 4. SQL Server Installation

- Install **Microsoft SQL Server 2019 Developer Edition**
- Install **SQL Server Management Studio (SSMS)**
- Enable TCP/IP via **SQL Server Configuration Manager**
- Create database: `BankDW`

---

## 📊 5. IBM Cognos Installation

- Download **IBM Cognos Analytics 11.2.x**
- Install on same server
- Configure Cognos Gateway to use IIS
- Create ODBC Data Source for SQL Server
- Test connection and publish to Cognos portal

---

## 🔐 6. Security Configuration

- Create local Windows users or integrate Active Directory
- Configure IIS authentication:
  - Windows Authentication (preferred)
  - Or Form-based login
- Use Cognos Admin Console to assign roles (Viewer, Author, Admin)

---

## 📎 Useful Tools

- Remote Desktop Connection
- IIS Manager
- SQL Server Management Studio
- Cognos Configuration Tool

---

## 📸 Screenshots Available

See `/screenshots/` folder in the root repository for setup validation

---

