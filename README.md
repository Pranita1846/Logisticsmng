# 🚚 B2B Logistics Management Platform

An **enterprise-grade, role-based B2B logistics management system** designed to handle end-to-end shipment operations including business onboarding, logistics planning, warehouse management, driver execution, photo-based verification, part-wise payments, and audited communication.

This project closely mirrors **real-world logistics platforms** used in the industry and is built for scalability, security, and operational transparency.

---

## 📌 Project Overview

The **B2B Logistics Management Platform** centralizes logistics operations by integrating:

- Businesses (shipment owners)
- Logistics Managers (planners & coordinators)
- Warehouses (mini WMS)
- Drivers (field execution)
- Admin (system authority)

into a **single controlled ecosystem** with strict role-based access and approval workflows.

---

## 🎯 Key Objectives

- Digitize and centralize logistics operations  
- Enable secure onboarding with admin verification  
- Provide real-time shipment tracking  
- Ensure accountability through photo verification  
- Enforce part-wise payment control  
- Reduce disputes using audit logs and chat history  
- Support scalable, multi-city logistics workflows  

---

## 👥 User Roles & Hierarchy

### Primary Roles
- **Admin**
- **Business**
  - Business Owner
  - Business Manager (Sub-user)
- **Logistics Manager**
- **Warehouse**
  - Warehouse Owner
  - Warehouse Manager
  - Warehouse Employee
- **Driver**

Each role has:
- A dedicated dashboard  
- Strict role-based permissions (RBAC)  

---

## 🔐 Authentication & Verification

### Registration Rules
- Business, Warehouse, and Driver → Self Registration  
- Logistics Manager → Created by Admin  
- Admin → System default  

### User Status Lifecycle
- `PENDING_VERIFICATION`
- `ACTIVE`
- `REJECTED`
- `SUSPENDED`

⚠️ Users cannot operate without admin approval.

---

## 🛠️ Admin Module (System Authority)

### Responsibilities
- Verify and approve:
  - Businesses
  - Warehouses
  - Drivers
- Create & manage **Logistics Manager accounts**
- Assign roles and permissions
- Suspend or deactivate users
- Monitor shipments (read-only)
- Monitor payments, invoices, and audit logs
- Handle disputes and compliance

---

## 🏢 Business Module (Shipment Owner)

### Business Owner Capabilities
- Register and upload legal documents
- Create shipment requests
- Define pickup, drop, and parcel details
- Track shipment lifecycle
- View photo verification logs
- Make **part-wise payments**
- Download invoices
- Add Business Managers (sub-users)

### Business Manager (Sub-user)
Can:
- Track shipments  
- View logs and photo proofs  
- Chat with Logistics Manager  

Cannot:
- Create or modify shipments  
- Make payments  
- Assign drivers or warehouses  

---

## 🧠 Logistics Manager Module (Planning & Control)

### Responsibilities
- Review and accept shipment requests
- Create end-to-end shipment execution plans
- Assign drivers and warehouses
- Monitor shipment execution
- Handle delays and operational exceptions

📌 Logistics Managers **do not handle payments**.

---

## 🚚 Driver Module (Shipment Execution)

### Driver Registration
- Self-registration
- Upload driving license & vehicle documents
- Admin verification required

### Driver Capabilities
- View assigned shipments only
- Accept or reject assignments
- Perform pickup, transport, and delivery
- Upload photos at every stage
- Enter OTP or signature at final delivery

🚫 Drivers cannot view payments or business details.

---

## 🏬 Warehouse Module (Mini WMS)

### Warehouse Roles

#### Warehouse Owner
- Registers warehouse
- Defines warehouse workflows
- Adds Warehouse Managers
- Views performance summaries

#### Warehouse Manager
- Manages daily operations
- Assigns tasks to employees
- Controls inbound & outbound flow
- Approves dispatch

#### Warehouse Employee
- Marks attendance
- Performs parcel handling tasks
- Updates daily work status

### Warehouse Workflow
1. Inbound receiving  
2. Inspection & photo verification  
3. Sorting & storage  
4. Dispatch approval  
5. Outbound handover  

---

## 📸 Photo-Based Verification

Mandatory photo uploads at:
- Pickup
- Warehouse inbound
- Damage inspection
- Dispatch
- Final delivery

Each photo includes:
- Timestamp
- Location
- Uploaded-by role
- Approval status

This ensures **dispute-free logistics operations**.

---

## 🤖 AI-Assisted Logistics Planning

AI acts as a **decision-support system**, providing:
- Route optimization suggestions
- Warehouse recommendations
- Driver availability & performance scoring
- Risk alerts for delays or high-value shipments

✔️ Final decisions remain with the **Logistics Manager**.

---

## 💳 Payment & Billing System

### Part-Wise Payment Model
1. After pickup  
2. Before inter-city transport  
3. Before final delivery  

🚫 Shipment progression is blocked if payment is pending.

### Billing
- Stage-wise invoice generation
- Final consolidated invoice after delivery

---

## 💬 Communication & Chat Module

### Allowed Communication
- Business Manager ↔ Logistics Manager
- Logistics Manager ↔ Warehouse Manager

🚫 Direct chat is not allowed between:
- Business ↔ Driver
- Business ↔ Warehouse
- Driver ↔ Warehouse Employee

### Chat Features
- Shipment-linked chat threads
- Timestamps & sender role visibility
- Read receipts (optional)
- Chat history stored for audit

Admin has **view-only access**.

---

## 🧾 Audit Logs & Compliance

Every system action is logged:
- User
- Role
- Timestamp
- Action performed

Used for:
- Audits
- Dispute resolution
- Performance analysis

---

## 🔄 Complete Shipment Lifecycle

