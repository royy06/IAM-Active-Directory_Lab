# IAM-Active-Directory_Lab
# 🛡️ Enterprise Active Directory & IAM Home Lab
**Role Simulation:** Junior Identity & Access Management (IAM) Administrator  
**Location:** Houston, TX (Lab Environment)  
**Tools:** Windows Server 2019, Oracle VirtualBox, Active Directory Domain Services (AD DS)

---

## 📋 Project Overview
This project demonstrates the end-to-end deployment of a Windows Server-based identity environment. I transitioned a standalone server into a Domain Controller, established a scalable Organizational Unit (OU) structure, and implemented security best practices including Role-Based Access Control (RBAC) and Group Policy governance.

---

## 🛠️ Phase 1: Infrastructure & Domain Setup

### Step 1: Server Provisioning & Static IP
* **The Action:** Configured Windows Server 2019 with a static IP address (`172.16.0.10`) and renamed the host to `DC01`.
* **The "Why":** Domain Controllers must have a static IP to ensure that DNS services and authentication requests from client machines never lose their connection to the server.

![Static IP Address](screenshots/Static%20IP%20Address.png)



### Step 2: AD DS Installation & Forest Promotion
* **The Action:** Installed the Active Directory Domain Services role and promoted the server to a Domain Controller for the `IAMLAB.local` forest.
* **The "Why":** Promoting the server creates the NTDS database, which acts as the centralized "brain" for all user identities and security permissions in the network.

![Log in Photo](screenshots/Log%20in%20Photo.png)


---

## 👤 Phase 2: Identity & Access Management (IAM)

### Step 3: Organizational Unit (OU) Design
* **The Action:** Designed a departmental hierarchy by creating OUs for `_Employees`, `HR`, `IT`, and `Finance`.
* **The "Why":** Proper OU design allows for "Delegated Administration." It enables us to apply specific security rules (GPOs) to one department without affecting others.

![User inside security group](screenshots/User%20inside%20security%20group.png)



### Step 4: User Provisioning & RBAC
* **The Action:** Created a test user (`John Doe`) and mapped them to a specific Security Group: `HR_Staff_SG`.
* **The "Why":** This follows **Role-Based Access Control (RBAC)**. Instead of giving John Doe individual permissions, we give the *Group* permissions. This makes it easier to "offboard" users or change permissions for entire departments instantly.


![OU Structure](screenshots/OU%20structure.png)




---

## 🔐 Phase 3: Security Governance & Data Protection

### Step 5: Enforcing Security Baselines (Group Policy)
* **The Action:** Used the Group Policy Management Console (GPMC) to enforce a **12-character minimum password length** domain-wide.
* **The "Why":** Centralized governance ensures that every user, regardless of department, follows company security standards to prevent "brute force" password attacks.

![Folder Security](screenshots/folder%20security%20tab.png)



### Step 6: NTFS Permissions (Least Privilege)
* **The Action:** Created a folder (`HR_Private`) and modified the security ACLs to grant "Modify" access only to the `HR_Staff_SG` group.
* **The "Why":** This implements the **Principle of Least Privilege**. Only users who *need* access to HR data for their jobs can see it; everyone else (including IT admins, ideally) is locked out.

![Password Policy](screenshots/password%20policy.png)


---

## 🎯 Key Takeaways for Interviewers
* **Identity Lifecycle:** I can manage the "Joiner-Mover-Leaver" process by provisioning users and managing groups.
* **Security First:** I understand how to enforce global security rules using Group Policy.
* **Data Integrity:** I know how to secure sensitive corporate data using NTFS permissions and group-based access.

