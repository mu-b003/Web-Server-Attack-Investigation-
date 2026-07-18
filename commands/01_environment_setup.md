# Environment Setup

This document contains all commands used to prepare the victim machine before the attack simulation.

---

## Update the System

```bash
sudo apt update
sudo apt upgrade -y
```

Purpose:

- Update package lists
- Install the latest security updates

---

## Install Apache

```bash
sudo apt install apache2 -y
```

Purpose:

- Install Apache Web Server

---

## Enable Apache

```bash
sudo systemctl enable apache2
```

---

## Start Apache

```bash
sudo systemctl start apache2
```

---

## Check Service Status

```bash
sudo systemctl status apache2
```

Expected Result:

- Apache service is active (running)

---

## Create the Test Website

```bash
cd /var/www/html
```

Remove the default page.

```bash
sudo rm index.html
```

Create fake web pages.

- index.html
- login.php
- admin.php
- upload.php
- config.php
- backup.zip

---

## Clear Apache Logs

```bash
sudo truncate -s 0 /var/log/apache2/access.log
```

```bash
sudo truncate -s 0 /var/log/apache2/error.log
```

Restart Apache.

```bash
sudo systemctl restart apache2
```

Purpose:

Prepare clean logs before the attack simulation.
