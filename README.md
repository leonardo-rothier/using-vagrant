# 2-Tier Application with Vagrant

This project sets up a **2-tier application** using **Vagrant**, provisioning two virtual machines:
- **Database VM**: Hosts the database service.
- **Web Server VM**: Runs a PHP-based web application.

## 📌 Project Structure
```
2-tier-application/
│-- db/              # Database VM configuration
│   ├── Vagrantfile  # Vagrant setup for database
│-- webserver/       # Web server VM configuration
│   ├── Vagrantfile  # Vagrant setup for web server
│-- .gitignore       # Ignore Vagrant-specific files
│-- README.md        # Project documentation
```

## 🚀 Getting Started
### 1️⃣ Install Dependencies
Ensure you have the following installed:
- [VirtualBox](https://www.virtualbox.org/)
- [Vagrant](https://www.vagrantup.com/)

### 2️⃣ Clone the Repository
```bash
git clone https://github.com/buluf/using-vagrant.git
cd using-vagrant/2-tier-application
```

### 3️⃣ Start the Virtual Machines
```bash
cd 2-tier-application/db
vagrant up

cd ../webserver
vagrant up
```
This will provision and configure both the **database** and **web server** VMs.

### 4️⃣ Access the WVMS
Once provisioning is complete, access the vms via:
```
ssh <vm_hostname>

```
or inside the vagrant dir

```
vagrant ssh

```

## ⚙️ Configuration
- The **database VM** runs **MySQL** (configured in `db/Vagrantfile`).
- The **web server VM** runs **PHP + Apache** (configured in `webserver/Vagrantfile`).
- Networking is set up so the web server can communicate with the database.

---
💡 **Contributions Welcome!** Feel free to fork, improve, and submit pull requests. 🚀
