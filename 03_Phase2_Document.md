# Phase 2: Org Setup & Configuration

## 1. Salesforce Editions
- The project is implemented on the **Salesforce Developer Edition org**, which provides free access for customization and testing.  
- For real-world deployment, **Enterprise Edition** would be preferred because it supports advanced features like profiles, roles, sharing rules, API integration, and sandbox creation.

## 2. Company Profile Setup
- Company profile set as **Student Accommodation Finder Pvt. Ltd.**  
- Details such as company name, address, primary contact, default currency (**INR**), and time zone configured.  

<img src="./Screenshots/Company%20profile.png" alt="Company Profile" width="500" style="border:2px solid #4CAF50; border-radius:10px;">

## 3. Business Hours & Holidays
- Business hours: **Monday–Saturday (9:00 AM – 7:00 PM)**  
- Public holidays (e.g., Independence Day, Diwali, New Year) added  

<img src="./Screenshots/Business%20hours.png" alt="Business Hours" width="500" style="border:2px solid #4CAF50; border-radius:10px;">

## 4. Fiscal Year Settings
- **Standard fiscal year** chosen (April–March)  

## 5. User Setup & Licenses
- Users created for roles: **Students, Landlords, Admins**  
- Licenses assigned:  
  - **Platform License** → Students and Landlords  
  - **Salesforce License** → Admins and Managers  

### Student User
<img src="./Screenshots/Student%20User.png" alt="Student User" width="500" style="border:2px solid #4CAF50; border-radius:10px;">

### Landlord User
<img src="./Screenshots/Landlord%20User.png" alt="Landlord User" width="500" style="border:2px solid #4CAF50; border-radius:10px;">

## 6. Profiles
- Profiles created to define baseline permissions:  
  - **Student Profile** – search, request, view accommodations  
  - **Landlord Profile** – list accommodations, update availability, view bookings  
  - **Admin Profile** – full access  

### Student Profile
<img src="./Screenshots/Student%20Profile.png" alt="Student Profile" width="500" style="border:2px solid #4CAF50; border-radius:10px;">

### Landlord Profile
<img src="./Screenshots/Landlord%20Profile.png" alt="Landlord Profile" width="500" style="border:2px solid #4CAF50; border-radius:10px;">

### Admin Profile
<img src="./Screenshots/System%20Administrator%20profile.png" alt="Admin Profile" width="500" style="border:2px solid #4CAF50; border-radius:10px;">

## 7. Roles
- Role hierarchy:  
  - **Admin** (top-level)  
  - **Landlord Manager**  
  - **Student Support Executive**  

### Student Role
<img src="./Screenshots/Student%20role.png" alt="Student Role" width="500" style="border:2px solid #4CAF50; border-radius:10px;">

### Landlord Role
<img src="./Screenshots/Landlord%20role.png" alt="Landlord Role" width="500" style="border:2px solid #4CAF50; border-radius:10px;">

### Admin Role
<img src="./Screenshots/Admin%20roles.png" alt="Admin Role" width="500" style="border:2px solid #4CAF50; border-radius:10px;">


## 8. Permission Sets
- Grant additional permissions without modifying profiles  
- Examples:  
  - Students → Read Accommodation, Create Booking  
  - Landlords → Manage Accommodation, Approve Bookings  
  - Admins → Full access  

### Student Permission Set
<img src="./Screenshots/Student permission sets.png" alt="Student Permission Set" width="500" style="border:2px solid #4CAF50; border-radius:10px;">

### Landlord Permission Set
<img src="./Screenshots/landlord permission sts.png" alt="Landlord Permission Set" width="500" style="border:2px solid #4CAF50; border-radius:10px;">

### Admin Permission Set
<img src="./Screenshots/admin permission sets.png" alt="Landlord Permission Set" width="500" style="border:2px solid #4CAF50; border-radius:10px;">

## 9. Organization-Wide Defaults (OWD)
- Booking → Private  
- Accommodation → Public Read/Write  
- Student → Private  
- Landlord → Private  

### Booking OWD
<img src="./Screenshots/booking Owd.png" alt="Booking OWD" width="500" style="border:2px solid #4CAF50; border-radius:10px;">

## 10. Sharing Rules
- Owner-Based: Bookings owned by Students → shared with Landlord → Read/Write  
- Criteria-Based: Bookings with Status = Confirmed → shared with Admin → Read/Write  
### Booking sharing rules
<img src="./Screenshots/Booking sharing rules.png" alt="Booking OWD" width="500" style="border:2px solid #4CAF50; border-radius:10px;">



## 11. Login Access Policies
- Enable admins temporary access for support  
### Login Access Settings
<img src="./Screenshots/login policies.png" alt="Booking OWD" width="500" style="border:2px solid #4CAF50; border-radius:10px;">



## 12. Developer Org Setup
- Sign up/Login at [developer.salesforce.com](https://developer.salesforce.com)  
- Create users: Students, Landlords, Admins  
- Create custom objects: Student__c, Landlord__c, Accommodation__c, Booking__c  
- App & Tab Setup: Booking, Accommodation, Student, Landlord  

## 13. Sandbox Usage
- Developer Edition does not include Sandbox; skipped  

## 14. Deployment Basics

### Salesforce CLI
```bash
  sfdx force:auth:web:login -a DevOrg
  sfdx force:source:pull
  sfdx force:auth:web:login -a TargetOrg
  sfdx force:source:push -u TargetOrg
