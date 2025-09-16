# Project Title: Student Accommodation Finder  
a website online platform that helps students find safe and affordable rooms when studying outside their hometown.  


## About the Project  

- **Project Name:** Student Accommodation Finder  
- **Platform:** Salesforce (Admin + Developer)  
- **Goal:** To create a centralized CRM-based solution where students can easily find affordable rooms, and landlords can list their properties securely.
- **Problem Statement:** Students who move to new cities for higher education face major challenges in finding safe, affordable, and reliable accommodation. They often depend on brokers, unverified listings, or informal channels, which leads to issues such as high rents, lack of security, and misinformation.The **Student Accommodation Finder** project aims to solve this problem by providing a centralized Salesforce-based platform that connects students with verified landlords, enabling transparency and ease of access.  

<br>

# Phase 1: Problem Understanding & Industry Analysis  

## 1. Problem Statement  
Students who move to new cities for higher education face major challenges in finding safe, affordable, and reliable accommodation. They often depend on brokers, unverified listings, or informal channels, which leads to issues such as high rents, lack of security, and misinformation.  
The **Student Accommodation Finder** project aims to solve this problem by providing a centralized Salesforce-based platform that connects students with verified landlords, enabling transparency and ease of access.  



## 2. Requirement Gathering  

### Functional Requirements  
- Students should be able to register and create profiles.  
- Students can search for rooms/hostels/PGs by city, price, facilities, and availability.  
- Landlords can register and list their rooms with details like rent, location, and facilities.  
- A booking system should allow students to request rooms.  
- Admin should approve and monitor listings.  
- Notifications (email/SMS) should be sent for bookings and approvals.  

### Non-Functional Requirements  
- Data security: Only authorized users can access data.  
- Performance: Search results should load quickly.  
- Usability: Interface should be simple for students and landlords.  
- Scalability: System should support multiple cities and thousands of listings.  



## 3. Stakeholder Analysis  

| Stakeholder     | Role in the System                                | Needs/Expectations                           |
|-----------------|---------------------------------------------------|----------------------------------------------|
| **Students**    | End users who search and book accommodation       | Easy search, affordable options, safety info |
| **Landlords**   | Provide rooms/PGs/hostels                         | Platform to list rooms and find tenants      |
| **Admin**       | Manages platform operations and approvals         | Control over data, monitor activities        |
| **Colleges**    | Optional stakeholders for future integration      | Verified housing options for students        |



## 4. Business Process Mapping  

**Step 1:** Student registers on the platform.  
**Step 2:** Student searches available rooms using filters (location, price, facilities).  
**Step 3:** Student selects a room and places a booking request.  
**Step 4:** Landlord receives notification and confirms availability.  
**Step 5:** Admin verifies and approves booking (if required).  
**Step 6:** Student receives confirmation email/SMS.  
**Step 7:** Feedback/complaint system allows students to rate their experience.  



## 5. Industry-Specific Use Case Analysis  

- **Education Industry:** Colleges want reliable housing solutions for their students.  
- **Real Estate Industry:** Property owners get a new market (students) without brokers.  
- **Technology/CRM Industry:** Salesforce provides a scalable, secure, and customizable platform for managing student-owner interactions.  

This project combines **EdTech + PropTech (Property Tech)** use cases.  



## 6. AppExchange Exploration  

Before custom development, we explored Salesforce AppExchange to check for existing solutions:  

- **Property Management Apps:** Designed for large-scale real estate companies, not student-focused.  
- **Rental Management Apps:** Expensive and more suited for commercial leasing.  
- **Education Apps:** Focused on learning, not accommodation.  

Conclusion: No AppExchange app currently solves this exact student accommodation problem, hence a **custom Salesforce solution** is required.  



## 7. Phase 1 Outcomes  

- Problem clearly defined: Lack of centralized, verified housing for students.  
- Requirements documented (functional + non-functional).  
- Stakeholders identified and mapped.  
- Business process flow created.  
- Industry gap validated (no direct AppExchange solution).  

  
<br>

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

![Company Profile Screenshot](./Student%20Accommodation%20Finder_Phases/Images/Company%20setup.png)


## 3️ Business Hours & Holidays
- **Business Hours:** Monday–Saturday, 9:00 AM – 7:00 PM (Accommodation Support Team).  
- **Holidays Added:** Independence Day, Diwali, New Year.  
- Prevents escalations or approvals during non-working days.  

![Company Profile Screenshot](./Student%20Accommodation%20Finder_Phases/Images/Business%20Hours.png)



## 4️ Fiscal Year Settings
- **Standard Fiscal Year (April–March)** chosen.  
- Aligns with Indian financial year standards.  
- Helps generate accurate financial reports for revenue & landlord payments.  

![Company Profile Screenshot](./Student%20Accommodation%20Finder_Phases/Images/Fiscal%20year.png)



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
