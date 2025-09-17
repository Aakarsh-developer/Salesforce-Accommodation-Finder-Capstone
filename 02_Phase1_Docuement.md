# Phase 1: Problem Understanding & Industry Analysis

## 1. Requirement Gathering

### Functional Requirements
- Students should be able to register and create profiles.  
- Students can search for rooms/hostels/PGs by city, price, facilities, and availability.  
- Landlords can register and list their rooms with details like rent, location, and facilities.  
- A booking system should allow students to request rooms.  
- Admin should approve and monitor listings.  
- Notifications (email/SMS) should be sent for bookings and approvals.  

### Non-Functional Requirements
- **Data security**: Only authorized users can access data.  
- **Performance**: Search results should load quickly.  
- **Usability**: Interface should be simple for students and landlords.  
- **Scalability**: System should support multiple cities and thousands of listings.  



## 2. Stakeholder Analysis

| **Stakeholder** | **Role in the System**                     | **Needs/Expectations**                               |
|-----------------|---------------------------------------------|------------------------------------------------------|
| Students        | End users who search and book accommodation | Easy search, affordable options, safety info         |
| Landlords       | Provide rooms/PGs/hostels                   | Platform to list rooms and find tenants              |
| Admin           | Manages platform operations and approvals   | Control over data, monitor activities                |
| Colleges        | Optional stakeholders for future integration| Verified housing options for students                |



## 3. Business Process Mapping

1. Student registers on the platform.  
2. Student searches available rooms using filters (location, price, facilities).  
3. Student selects a room and places a booking request.  
4. Landlord receives notification and confirms availability.  
5. Admin verifies and approves booking (if required).  
6. Student receives confirmation email/SMS.  
7. Feedback/complaint system allows students to rate their experience.  


## 4. Industry-Specific Use Case Analysis

- **Education Industry**: Colleges want reliable housing solutions for their students.  
- **Real Estate Industry**: Property owners get a new market (students) without brokers.  
- **Technology/CRM Industry**: Salesforce provides a scalable, secure, and customizable platform for managing student-owner interactions.  


## 5. AppExchange Exploration

Before custom development, we explored Salesforce AppExchange to check for existing solutions:  

- **Property Management Apps**: Designed for large-scale real estate companies, not student-focused.  
- **Rental Management Apps**: Expensive and more suited for commercial leasing.  
- **Education Apps**: Focused on learning, not accommodation.  


