# Lab 3: Active Directory Domain-Join & Hostname Standardization

## 🎯 Objective
To securely onboard newly refreshed workstation endpoints into a centralized management framework. This lab demonstrates how to establish an enterprise device identity standard, join a client computer to a local Active Directory domain controller, and position it within a secure Organizational Unit (OU) structure.

## 🧠 Technical Thought Process & Code Architecture

### 1. Identity & Access Strategy (The Big Picture)
* **Assessment:** Unmanaged standalone computers present a critical security risk. New or refreshed machines must instantly fall under central management to receive security policies, network access controls, and proper user permissions.
* **Infrastructure Focus:** This lab focuses on directory architecture. By standardizing physical device placement into clean Organizational Units (OUs), the enterprise can safely scale and apply security settings seamlessly.

### 2. Step-by-Step Configuration Breakdown
Below is the precise deployment logic for each critical milestone in the configuration phase:

* **Step:** *Implementing Corporate Hostname Conventions (e.g., `NYC-LHP-0042` via Windows System Settings)*
  * **Technical Meaning:** Renames the local computer object from its random default name to a structured asset tag layout before domain registration.
  * **Operational Reasoning:** Allows IT infrastructure teams to instantly identify a machine's physical location (`NYC`), device type (`LHP` for Laptop), and specific asset number (`0042`) from any monitoring dashboard.
* **Step:** *Executing the Domain Join Linkage (`company.local` configuration)*
  * **Technical Meaning:** Authenticates the local device client against the Domain Controller's DNS server and creates an active secure channel with the Active Directory Database.
  * **Operational Reasoning:** Shifts the computer from a weak local authentication model to centralized authentication, ensuring the user can log in securely using their corporate credentials.
* **Step:** *Staging the Computer Object into a Dedicated Departmental OU*
  * **Technical Meaning:** Moves the registered computer object out of the default "Computers" container and drops it into a structured target folder (like `IT_Hardware` or `HR_Devices`).
  * **Operational Reasoning:** Ensures that Group Policy Objects (GPOs)—such as mandatory firewalls, corporate wallpapers, or security settings—automatically deploy to the machine based on the employee's job function.

## 📸 Visual Verification & Proof of Work
*[Insert your screenshot here showing your computer object listed cleanly inside its assigned Organizational Unit folder within the Active Directory Users and Computers console]*
