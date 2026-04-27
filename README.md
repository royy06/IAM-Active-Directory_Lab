# IAM-Active-Directory_Lab
# Windows Server 2019 IAM & Active Directory Lab

## 📌 Project Overview
This project demonstrates the setup and configuration of a Windows Server 2019 environment within a VirtualBox virtual machine. The goal of this lab is to simulate a corporate infrastructure focusing on Identity and Access Management (IAM), Active Directory Domain Services (AD DS), and Organizational Unit (OU) structures for departments like HR, IT, and Finance.

## 🛠 Tech Stack
* **Hypervisor:** Oracle VirtualBox
* **Operating System:** Windows Server 2019 Standard (Desktop Experience)
* **Services:** Active Directory Domain Services (AD DS), DNS

## 🚀 Phase 1: Virtual Environment Setup
1.  **Virtual Machine Configuration:** * Name: `DC01-IAMLAB`
    * RAM: 4GB
    * CPU: 2 Cores
    * Storage: 50GB VDI (Dynamically Allocated)
2.  **Hardware Optimization:** Enabled **VT-x (Virtualization Technology)** in the physical host BIOS to support 64-bit virtualization.
3.  **OS Installation:** Performed a clean manual installation of Windows Server 2019 using an ISO image, specifically selecting the **Desktop Experience** to allow for GUI management.

## 📁 Active Directory Structure (Planned)
The lab is designed to simulate a real-world company hierarchy:
* **Root Domain:** `IAMLAB.local` (Planned)
* **Organizational Units (OUs):**
    * 🏢 **Finance** (Users, Groups, Permissions)
    * 👨‍💻 **IT** (Administrative accounts)
    * 🤝 **HR** (Onboarding/Offboarding simulation)

## 📸 Progress Screenshots
*(Tip: Upload your screenshots to a folder named /img in your repo and link them here)*
![Server Login Screen](./img/login_screen.png)

## 💡 Key Learnings
* Configuring BIOS/UEFI settings for virtualization.
* Managing virtual hardware resources.
* Windows Server installation and Administrator account security.

