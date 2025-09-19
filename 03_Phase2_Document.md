# Phase 2: Org Setup & Configuration
## 1. Salesforce Editions
- The project is implemented on the **Salesforce Developer Edition org**, which provides free access for customization and testing.  
- For real-world deployment, **Enterprise Edition** would be preferred because it supports advanced features like profiles, roles, sharing rules, API integration, and sandbox creation.



## 2. Company Profile Setup
- Company profile set as **Student Accommodation Finder Pvt. Ltd.**  
- Details such as company name, address, primary contact, default currency (**INR**), and time zone configured.  
- This ensures that all business processes in Salesforce reflect the organization’s identity.  

<img src="./Screenshots/Company%20profile.png" alt="Company Profile" width="500" style="border:2px solid #4CAF50; border-radius:10px;">



## 3. Business Hours & Holidays
- Business hours configured as **Monday–Saturday (9:00 AM – 7:00 PM)** to reflect accommodation support team availability.  
- Public holidays (e.g., Independence Day, Diwali, New Year) added to avoid escalations or booking approvals on non-working days.  

<img src="./Screenshots/Business%20hours.png" alt="Business Hours" width="500" style="border:2px solid #4CAF50; border-radius:10px;">



## 4. Fiscal Year Settings
- **Standard fiscal year** chosen (April–March) to align with Indian financial year standards.  
- Helps in generating financial reports for accommodation revenue and landlord payments.  



## 5. User Setup & Licenses
- Users created for different roles: **Students, Landlords, Admins**.  
- Each user assigned an appropriate Salesforce license:  
  - **Platform License** → Students and Landlords.  
  - **Salesforce License** → Admins and Managers.  
- Profiles and permission sets used to define user access levels.  

###   Student User
<img src="./Screenshots/Student%20User.png" alt="Student User" width="500" style="border:2px solid #4CAF50; border-radius:10px;">

### - Landlord User
<img src="./Screenshots/Landlord%20User.png" alt="Landlord User" width="500" style="border:2px solid #4CAF50; border-radius:10px;">



## 6. Profiles
- Profiles created to define baseline permissions:  
  - **Student Profile** – can search, request, and view accommodations.  
  - **Landlord Profile** – can list accommodations, update availability, and view booking requests.  
  - **Admin Profile** – full access to manage users, approvals, and data.  

### - Student Profile
<img src="./Screenshots/Student%20Profile.png" alt="Student Profile" width="500" style="border:2px solid #4CAF50; border-radius:10px;">

### Landlord Profile
<img src="./Screenshots/Landlord%20Profile.png" alt="Landlord Profile" width="500" style="border:2px solid #4CAF50; border-radius:10px;">

### Admin Profile
<img src="./Screenshots/System%20Administrator%20profile.png" alt="Admin Profile" width="500" style="border:2px solid #4CAF50; border-radius:10px;">



## 7. Roles
- Role hierarchy defined to control data visibility:  
  - **Admin** (top-level)  
  - **Landlord Manager**  
  - **Student Support Executive**  
- Roles ensure that landlords only see their own listings and students only see available accommodations.  

### Student Role
<img src="./Screenshots/Student%20role.png" alt="Student Role" width="500" style="border:2px solid #4CAF50; border-radius:10px;">

### Landlord Role
<img src="./Screenshots/Landlord%20role.png" alt="Landlord Role" width="500" style="border:2px solid #4CAF50; border-radius:10px;">

### Admin Role
<img src="./Screenshots/Admin%20roles.png" alt="Admin Role" width="500" style="border:2px solid #4CAF50; border-radius:10px;">
