<div align="center">

# ☁️ WordPress Infrastructure on AWS

### Deploying a Production-Ready WordPress Website Using Amazon EC2 and Amazon RDS (MySQL)

![AWS](https://img.shields.io/badge/AWS-Cloud-orange?style=for-the-badge&logo=amazonaws)
![EC2](https://img.shields.io/badge/Amazon-EC2-FF9900?style=for-the-badge)
![RDS](https://img.shields.io/badge/Amazon-RDS-527FFF?style=for-the-badge)
![WordPress](https://img.shields.io/badge/WordPress-CMS-21759B?style=for-the-badge&logo=wordpress)
![Apache](https://img.shields.io/badge/Apache-Web%20Server-D22128?style=for-the-badge&logo=apache)
![PHP](https://img.shields.io/badge/PHP-8.5-777BB4?style=for-the-badge&logo=php)
![Linux](https://img.shields.io/badge/Linux-Amazon%20Linux-yellow?style=for-the-badge&logo=linux)

</div>

---

# 📖 Project Overview

This project demonstrates how to deploy a **WordPress website** on **Amazon Web Services (AWS)** using **Amazon EC2** as the web server and **Amazon RDS (MySQL)** as the managed database.

The web server runs on **Amazon Linux 2023** with **Apache HTTP Server** and **PHP**, while **Amazon RDS** provides a secure and scalable MySQL database backend. This architecture follows AWS best practices by separating the application and database layers.

---

# 🏗️ Architecture

```text
                     Internet
                          │
                    Public IP Address
                          │
                 +----------------------+
                 |      Amazon EC2      |
                 | Apache + PHP         |
                 | WordPress Website    |
                 +----------+-----------+
                            │
                     MySQL Port 3306
                            │
                 +----------▼-----------+
                 |     Amazon RDS       |
                 |        MySQL         |
                 | WordPress Database   |
                 +----------------------+
```

---

# ☁️ AWS Services Used

- Amazon EC2
- Amazon RDS (MySQL)
- Amazon VPC
- Security Groups
- Internet Gateway
- Amazon Linux 2023
- Apache HTTP Server
- PHP
- MariaDB Client
- WordPress

---

# 🚀 Features

- WordPress hosted on Amazon EC2
- Amazon RDS MySQL Database
- Secure EC2 to RDS Connectivity
- Apache Web Server
- PHP Runtime
- WordPress Installation Wizard
- Live WordPress Website
- Production-ready Cloud Infrastructure

---

# 🛠️ Implementation Steps

## Step 1 – Launch Amazon EC2

- Amazon Linux 2023
- Configure Security Group
- Allow SSH (22)
- Allow HTTP (80)

---

## Step 2 – Install Apache & PHP

```bash
sudo dnf install httpd -y
sudo systemctl enable httpd
sudo systemctl start httpd

sudo dnf install php php-mysqlnd php-fpm php-json php-gd php-mbstring php-xml -y
```

---

## Step 3 – Download and Configure WordPress

```bash
wget https://wordpress.org/latest.tar.gz

tar -xvf latest.tar.gz

sudo cp -r wordpress/* /var/www/html/
```

---

## Step 4 – Create Amazon RDS

- Engine: MySQL
- Configure Database
- Allow Port 3306
- Create WordPress Database

---

## Step 5 – Install MariaDB Client

```bash
sudo dnf install mariadb105 -y
```

---

## Step 6 – Connect EC2 to Amazon RDS

```bash
mysql -h <RDS-ENDPOINT> -u admin -p
```

---

## Step 7 – Create WordPress Database

```sql
CREATE DATABASE wordpress;

SHOW DATABASES;
```

---

## Step 8 – Configure WordPress

Update the **wp-config.php** file with your RDS database details and complete the WordPress installation.

---

# 📸 Project Screenshots

## 🔗 EC2 Connected to Amazon RDS

The Amazon EC2 instance successfully connects to the Amazon RDS MySQL database using the MariaDB client.

<img src="ec2-rds-database-connection.png" width="100%">

---

## 🗄️ WordPress Database Created

A dedicated **WordPress** database is created inside Amazon RDS and verified using the SQL `SHOW DATABASES;` command.

<img src="wordpress-database-created.png" width="100%">

---

## 🎉 WordPress Installation Completed

The WordPress installation wizard has completed successfully, confirming that the application is correctly configured and ready to use.

<img src="wordpress-installation-success.png" width="100%">

---

## 🌐 Live WordPress Website

Final output of the deployed WordPress website running successfully on Amazon EC2 with Amazon RDS as its backend database.

<img src="wordpress-homepage.png" width="100%">

---

# 📁 Project Structure

```text
wordpress-infrastructure-on-aws/
│
├── README.md
├── ec2-rds-database-connection.png
├── wordpress-database-created.png
├── wordpress-installation-success.png
└── wordpress-homepage.png
```

---

# 🎯 Skills Demonstrated

- AWS EC2
- Amazon RDS (MySQL)
- WordPress Deployment
- Apache HTTP Server
- PHP
- Linux Administration
- MariaDB Client
- VPC
- Security Groups
- Cloud Infrastructure

---

# 📚 Learning Outcomes

- Successfully deployed WordPress on Amazon EC2.
- Installed and configured Apache and PHP.
- Connected Amazon EC2 to Amazon RDS.
- Created and configured a MySQL database on Amazon RDS.
- Completed the WordPress installation process.
- Hosted a live WordPress website using AWS services.
- Gained hands-on experience with cloud infrastructure and Linux administration.

---

# 👨‍💻 Author

**Dineshkumar R**

**Aspiring AWS Cloud & DevOps Engineer**

- **GitHub:** https://github.com/dineshkumarrp22-ops
- **LinkedIn:** www.linkedin.com/in/dinesh-kumar-engr

---

<div align="center">

### ⭐ If you found this project helpful, please give it a Star!

🚀 **Thank you for visiting my repository!**

</div>
