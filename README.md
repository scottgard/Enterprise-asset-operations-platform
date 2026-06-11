
# Enterprise Asset Operations Platform

A modern enterprise-grade asset management solution built using Microsoft Power Platform and Azure services.

---

## 🚀 Project Overview

The **Enterprise Asset Operations Platform** is a cloud-based application designed to help organisations manage physical assets, inspections, service jobs, maintenance, and inventory — all in one place.

In a lot of environments, these processes are still handled using spreadsheets or disconnected systems. That leads to poor visibility, manual work, and difficulty tracking what's actually happening operationally.

This project was built to solve that problem by creating a **centralised, scalable, and automated platform** using the Microsoft ecosystem.

---

## ✨ Core Features

### Asset Management
- Centralised asset register  
- Full lifecycle tracking (Available, Assigned, Under Maintenance, Retired)  
- Location and ownership management  

### Asset Details & History
- Detailed asset view  
- Linked inspections and service jobs  
- Visibility of asset value and usage  

### Inspection Tracking
- Inspection logging with condition tracking:
  - Good  
  - Minor Issue  
  - Major Issue  
  - Unsafe  
- Issue summaries and history  
- Helps identify risk and maintenance needs  

### Service Job Management
- Track repair and maintenance work  
- Job statuses:
  - Open  
  - In Progress  
  - Completed  
  - On Hold  
- Linked directly to assets  

### Inventory Management
- Track stock levels and usage  
- Highlight low stock and out-of-stock items  
- Supports maintenance and service operations  

### Dashboard & KPI Reporting
- Real-time operational dashboard  
- KPIs include:
  - Total assets  
  - Inspection counts  
  - Major issues  
  - Open service jobs  
  - Inventory levels  
- Includes summary breakdowns and recent activity tracking  

### Azure Blob Storage Integration
- Stores asset photos outside of Dataverse  
- Helps keep the app scalable  
- Secure and efficient file handling  

### Search & Filtering
- Search across assets, inspections, and jobs  
- Filter by status, category, and location  
- Designed to work with large datasets  

### Role-Based Access
- Different views depending on user role  
- Secure access using Microsoft 365 identity  

### Automated Workflows
- Built using Power Automate  
- Handles:
  - Notifications  
  - Status updates  
  - Maintenance triggers  

---

## 🛠 Technology Stack

| Technology | Purpose |
|----------|--------|
| Power Apps (Canvas App) | Front-end application |
| Microsoft Dataverse | Data storage and relationships |
| Power Automate | Workflow automation |
| Azure Blob Storage | Image storage |
| Microsoft 365 | Authentication and integration |
| Power Fx | App logic |

---

## 🏗 Architecture

User
↓
Power Apps (Canvas App)
↓
Dataverse (Data Layer)
↓
Power Automate (Workflow Layer)
↓
Azure Blob Storage (Images)
↓
Microsoft 365 (Authentication & Security)

---

## 🧩 Architecture Diagram

<img width="706" height="131" alt="image" src="https://github.com/user-attachments/assets/e52842a9-f234-4dec-b304-2df0beef72a1" />

---

The app is built using a fairly standard Power Platform architecture, but designed with scalability in mind.

Users interact with the Power Apps front end, which connects directly to Dataverse where all the structured data lives.

Power Automate runs in the background handling business logic and automation, while Azure Blob Storage is used for storing images instead of putting that load into Dataverse.

Authentication and access are handled through Microsoft 365, keeping everything secure and consistent with enterprise environments.

---

## 🧱 Data Model

<img width="706" height="131" alt="image" src="https://github.com/user-attachments/assets/b58374d9-8774-444e-ae54-87f21e656472" />

---

The data model is centred around the **Assets** table.

- Each asset can have multiple **inspections**  
- Each asset can also have multiple **service jobs**  
- **Inventory** links into service jobs to represent parts usage  

This structure keeps things clean and flexible, which is important when you start scaling or adding new features later.

---

## 📊 Screens

### Dashboard
<img width="1377" height="773" alt="image" src="https://github.com/user-attachments/assets/ff95d471-d3cf-4483-8b83-a0da33f8b135" />


### Asset Management
./images/assets.png

### Asset Details
<img width="1377" height="775" alt="image" src="https://github.com/user-attachments/assets/da30d607-b6fb-45a4-90ae-efb674e831ad" />


### Add Asset
<img width="1376" height="776" alt="image" src="https://github.com/user-attachments/assets/4b109e0e-b507-43f5-bc9f-e75c7c25f819" />


### Inspections
<img width="1373" height="773" alt="image" src="https://github.com/user-attachments/assets/3b9ee791-fb18-4c60-90a5-d09bddf50f49" />


### Service Jobs
<img width="1380" height="778" alt="image" src="https://github.com/user-attachments/assets/05677250-ff37-464b-b62e-34c34fe225a7" />


### Inventory
<img width="1371" height="773" alt="image" src="https://github.com/user-attachments/assets/d8a752cd-1ac8-42a9-ab3d-e0b0b18fd267" />


---

## 💡 Key Skills Demonstrated

- Power Apps Canvas App Development  
- Dataverse Data Modelling & Relationships  
- Azure Integration (Blob Storage)  
- Power Automate Workflow Automation  
- Responsive UI Design  
- KPI Dashboard Development  
- Business Process Analysis  
- Enterprise Application Build  

---

## ⚡ Challenges & Solutions

### Integrating Azure Blob Storage
Storing images directly in Dataverse isn't ideal at scale.

**Solution:**
- Used Power Automate to upload images to Azure Blob Storage  
- Stored file references back in Dataverse  

---

### Managing Dataverse Relationships
With multiple connected entities, things can get messy quickly.

**Solution:**
- Designed a clean relational model using lookup columns  
- Ensured clear ownership between tables  

---

### Building a Scalable Data Model
Needed something that could grow beyond a basic demo.

**Solution:**
- Normalised tables  
- Created reusable entity structures  
- Kept relationships clean and extendable  

---

### Performance Optimisation
Large datasets can slow down Power Apps if not handled properly.

**Solution:**
- Used delegation-friendly queries  
- Applied efficient filtering  
- Reduced unnecessary data loading  

---

## 🔮 Future Improvements

- QR / Barcode scanning for assets  
- Power BI integration for reporting  
- Mobile-first UI improvements  
- Predictive maintenance tracking  
- Multi-site asset management  
- Automated scheduling for service jobs  

---

## 💼 Business Impact

This solution helps organisations:

- ✅ Improve asset visibility  
- ✅ Reduce manual administrative work  
- ✅ Track maintenance more effectively  
- ✅ Centralise operational data  
- ✅ Make faster, better decisions  

---

## 🎬 Demo

### Screenshots
See above sections.

### Demo Walkthrough
A quick walkthrough showing asset search, viewing details, and editing.

<img width="400" height="226" alt="image" src="https://github.com/user-attachments/assets/ff676248-db70-40b6-99b3-934d53cd1d5f" />

---


## 📁 Project Structure

This project is built within the Microsoft Power Platform, so rather than a traditional codebase, it consists of:

- Power Apps Canvas App (UI & logic)
- Dataverse Tables (data model)
- Power Automate Flows (automation)
- Azure Blob Storage (image handling)

---

## 👨‍💻 Author

**Scott Gardner**  
Power Platform Developer  
Azure & Microsoft 365 Enthusiast  

GitHub: https://github.com/scottgard

