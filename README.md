# 💼 Data Warehousing & Reporting POC for Banking Sector (Azure + Cognos + SQL Server)

This repository presents a complete Proof of Concept (POC) for a business intelligence and data mining solution tailored to the Canadian banking and financial services sector.  
It integrates Microsoft SQL Server, IBM Cognos Analytics, IIS, and Windows Server 2019, all deployed on Microsoft Azure.

---

## 🎯 Objective

Deliver a cloud-hosted analytics solution that allows banking institutions to:

- Track transaction volumes by branch, region, and product
- Detect anomalies or high-risk customer behavior
- Provide dashboards for analysts, finance teams, and compliance officers

---

## 🏗️ Architecture Overview

[CSV Source Data]
↓
[SQL Server 2019 on Azure VM]
↓
[ODBC Connection]
↓
[IBM Cognos Analytics on IIS]
↓
[Secure Web Portal for Users]


---

## 🧰 Technology Stack

| Component                    | Version          | Role                                 |
|-----------------------------|------------------|--------------------------------------|
| Windows Server              | 2019 Datacenter  | OS hosting SQL Server & Cognos       |
| Microsoft SQL Server        | 2019 Developer   | Data warehouse (BankDW)              |
| SQL Query Language          | T-SQL            | Data ingestion, views, reporting     |
| IBM Cognos Analytics        | 11.2.x           | Reports and dashboards               |
| IIS (Internet Information Services) | 10       | Cognos Web Hosting                   |
| Azure Virtual Machine       | Standard_D2s_v3  | Hosting the full solution            |

---

## 🚀 Features

- 📊 Interactive reports (by product, region, branch)
- 🔍 Fraud detection simulation using customer profiles
- 👥 Secure access roles via Cognos & IIS
- 🌐 Web-accessible reporting via IIS

---

## 🧪 Sample Reports

- **Transaction volume by branch and type**
- **Customer segmentation by risk profile**
- **Inactive product detection (low volume accounts)**

Screenshots available in `/screenshots/`

---

## 🗂️ Folder Structure

📁 data/ → Sample CSVs (clients, transactions, products)
📁 sql/ → SQL scripts for DB setup
📁 cognos/ → Framework Manager model, report screenshots
📁 iis_config/ → Web.config for IIS deployment
📁 azure/ → VM & Windows setup guides
📁 screenshots/ → UI and setup captures
📄 README.md → This file


---

## 📸 Screenshots

![Azure VM Setup](screenshots/azure-vm-creation.png)  
*Azure VM with Windows Server 2019*

![IIS Setup](screenshots/iis-role-installation.png)  
*IIS configuration with ASP.NET for Cognos*

![Cognos Reports](screenshots/cognos-report-builder.png)  
*Banking dashboard in Cognos Analytics*

---

## 🛠️ Setup Guide

1. Create Azure VM with Windows Server 2019  
2. Install SQL Server + SSMS → Configure database  
3. Install Cognos Analytics and configure ODBC connection  
4. Deploy Cognos via IIS  
5. Build and publish reports  
6. Secure access and test user flows

➡ See [`azure/windows_server_2019_setup.md`](azure/windows_server_2019_setup.md)

---

## 📄 License

MIT License
