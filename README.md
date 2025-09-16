#  Student Accommodation Finder – Affordable Housing CRM  

##  Industry  
Real Estate / Education Services  

##  Project Type  
B2C Salesforce CRM Implementation  

##  Target Users  
- Students  
- Property Owners  
- Customer Support Agents  
- Managers  

---

##  Problem Statement  
Many students studying outside their hometown struggle to find affordable and reliable accommodations. Current processes are fragmented:  
- Students rely on multiple third-party apps, word of mouth, or brokers.  
- Property availability, pricing, and amenities are not transparent.  
- There’s no proper request tracking for booking, complaints, or cancellations.  
- Support agents manually assign cases leading to delays.  
- Managers lack visibility into demand trends, property occupancy rates, and service quality.  

The company wants a **Salesforce CRM solution** to:  
- Automate booking and complaint management.  
- Maintain centralized student and property records.  
- Provide real-time notifications (SMS/Email) to students.  
- Offer a **self-service portal** for students to search and request rooms.  
- Enable managers to track occupancy, complaints, and service performance.  

---

##  Use Cases  

### 1. Student Management  
- Maintain centralized student profiles with contact info and current accommodation details.  
- Track active and past bookings linked with each student.  

### 2. Property & Room Management  
- Store property details: **Name, Location, Room Type (Single/Shared), Rent, Facilities**.  
- Link available rooms to their respective property owners.  
- Automatically update room status (**Available → Booked → Vacant**).  

### 3. Booking & Complaint Requests  
- Students raise **booking requests** for available rooms.  
- Students can raise **complaint requests** (maintenance, cleanliness, facilities).  
- Requests automatically assigned to agents based on availability.  
- Agents update request status (**Open → In Progress → Closed**).  

### 4. Booking Confirmation & Cancellation  
- On booking confirmation → CRM auto-sends SMS/Email with details.  
- On cancellation → Room status is auto-updated to **Vacant**.  

### 5. Reporting & Analytics  
- **Reports:** Bookings by Property, Complaints by Type/Priority.  
- **Dashboard:** Occupied vs Vacant Rooms (Occupancy Analysis).  
- **Student Trends:** Active students, cancelled bookings.  
- **Agent Performance:** Requests resolved per agent.  
  

---

## 🛠️ Tech Stack  
- **Salesforce CRM** (Service Cloud + Experience Cloud)  
- **Custom Objects:** Student, Property, Room, Booking, Complaint  
- **Automation:** Assignment Rules, Flows for booking confirmation & cancellation  
- **Notifications:** Email & SMS Alerts  
- **Dashboards & Reports:** For occupancy, booking, and complaints  

