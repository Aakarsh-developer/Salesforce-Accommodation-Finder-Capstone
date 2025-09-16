# Phase 2: Org Setup & Configuration

This phase focuses on setting up and configuring the Salesforce Org for the **Student Accommodation Finder** project.  
The configurations ensure smooth operations, security, and scalability for the application.



## 1️ Salesforce Editions
- Implemented on **Salesforce Developer Edition Org** (free access for customization and testing).  
- For real-world deployment, **Enterprise Edition** is preferred because it supports:  
  - Profiles & Roles  
  - Sharing Rules  
  - API Integration  
  - Sandbox Creation  



## 2️ Company Profile Setup
- Company Profile set as **Student Accommodation Finder Pvt. Ltd.**  
- Configured details:  
  - Company Name, Address, Primary Contact  
  - Default Currency: **INR**  
  - Time Zone: **Asia/Kolkata**  
- Ensures Salesforce reflects the organization’s identity in all processes.  

![Company Profile Screenshot](/Project_Document/Images/Company%20setup.png)


## 3️ Business Hours & Holidays
- **Business Hours:** Monday–Saturday, 9:00 AM – 7:00 PM (Accommodation Support Team).  
- **Holidays Added:** Independence Day, Diwali, New Year.  
- Prevents escalations or approvals during non-working days.  

![Company Profile Screenshot](/Project_Document/Images/Business%20Hours.png)



## 4️ Fiscal Year Settings
- **Standard Fiscal Year (April–March)** chosen.  
- Aligns with Indian financial year standards.  
- Helps generate accurate financial reports for revenue & landlord payments.  

![Company Profile Screenshot](/Project_Document/Images/Fiscal%20year.png)



## 5️ User Setup & Licenses
- Users created for different roles:  
  - **Students, Landlords, Admins**  
- License assignment:  
  - **Platform License →** Students & Landlords  
  - **Salesforce License →** Admins & Managers  
- **Profiles & Permission Sets** used for access control.  



## 6️ Profiles
- **Student Profile:** Search, request, and view accommodations.  
- **Landlord Profile:** List accommodations, update availability, view booking requests.  
- **Admin Profile:** Full access to manage users, approvals, and data.  



## 7️ Roles
Defined role hierarchy to control visibility:  
- **Admin (Top-level)**  
- **Landlord Manager**  
- **Student Support Executive**  

Ensures:  
- Landlords see only their listings.  
- Students see only available accommodations.  



## 8️ Permission Sets
Used to extend access without modifying profiles:  
- **Booking Manager →** Handle booking approvals.  
- **Reporting Access →** View dashboards and analytics.  



## 9️ Organization-Wide Defaults (OWD)
- **Accommodation Object → Private** (only landlord can view/edit own properties).  
- **Booking Object → Controlled by Parent**.  
- **Student Object → Private** (students manage only their profiles).  



##  Sharing Rules
- Students can view accommodations marked as **Available**.  
- Admins → **Read/Write** access to all records.  
- Landlords → Share specific listings with students upon request.  



## 1️1️ Login Access Policies
- Enforced **Password Policies** (length, complexity, expiration).  
- **Login IP Ranges** restricted for Admin users.  
- **Two-Factor Authentication (2FA)** enabled for Admins & Landlords.  



## 1️2️ Developer Org Setup
- Developer Org created for:  
  - **Custom Objects:** Student, Landlord, Accommodation, Booking  
  - **Apex Classes** & Metadata  
- Serves as foundation for sandbox creation & deployments.  



## 1️3️ Sandbox Usage
- **Developer Sandbox** used for testing customizations.  
- **Data Masking** applied for student privacy.  
- **QA Team** uses sandbox for testing workflows & approval processes.  



## 1️4️ Deployment Basics
- **Deployment Flow:** Developer Org → Sandbox → Production.  
- Tools used:  
  - **Change Sets** → Configuration & Metadata migration  
  - **SFDX CLI & VS Code** → Advanced deployments  
- Ensures features (e.g., Feedback System, Payment Gateway) are tested before release.  
