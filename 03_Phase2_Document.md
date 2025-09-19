# Phase 2: Org Setup & Configuration

## 1. Salesforce Editions
- The project is implemented on the **Salesforce Developer Edition org**, which provides free access for customization and testing.  
- For real-world deployment, **Enterprise Edition** would be preferred because it supports advanced features like profiles, roles, sharing rules, API integration, and sandbox creation.



## 2. Company Profile Setup
- Company profile set as **Student Accommodation Finder Pvt. Ltd.**  
- Details such as company name, address, primary contact, default currency (**INR**), and time zone configured.  
- This ensures that all business processes in Salesforce reflect the organization’s identity.  
![Company Profile](./Screenshots/Company%20profile.png)




## 3. Business Hours & Holidays
- Business hours configured as **Monday–Saturday (9:00 AM – 7:00 PM)** to reflect accommodation support team availability.  
- Public holidays (e.g., Independence Day, Diwali, New Year) added to avoid escalations or booking approvals on non-working days.
![Business Hours](./Screenshots/Business%20hours.png)




## 4. Fiscal Year Settings
- **Standard fiscal year** chosen (April–March) to align with Indian financial year standards.  
- Helps in generating financial reports for accommodation revenue and landlord payments.  



## 5. User Setup & Licenses
- Users created for different roles: **Students, Landlords, Admins**.  
- Each user assigned an appropriate Salesforce license:  
  - **Platform License** → Students and Landlords.  
  - **Salesforce License** → Admins and Managers.  
- Profiles and permission sets used to define user access levels. 

### Student User
![Student Users](./Screenshots/Student%20User.png)

### Landlord User
![Landlord User](./Screenshots/Landlord%20User.png)





## 6. Profiles
- Profiles created to define baseline permissions:  
  - **Student Profile** – can search, request, and view accommodations.  
  - **Landlord Profile** – can list accommodations, update availability, and view booking requests.  
  - **Admin Profile** – full access to manage users, approvals, and data. 
### Student Proifle
![Student Profile](./Screenshots/Student%20Profile.png)
### Landlord Profile
![Company Profile](./Screenshots/Landlord%20Profile.png)
### Admin Profile
![Admin Profile](./Screenshots/System%20Administrator%20profile.png)


## 7. Roles
- Role hierarchy defined to control data visibility:  
  - **Admin** (top-level)  
  - **Landlord Manager**  
  - **Student Support Executive**  
- Roles ensure that landlords only see their own listings and students only see available accommodations.  
### Student Role
![Student Role](./Screenshots/Student%20role.png)
### Landlord Role
![Landlord Role](./Screenshots/Landlord%20role.png)
### Admin Role
![Admin Role](./Screenshots/Admin%20roles.png)

