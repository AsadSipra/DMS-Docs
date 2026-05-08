# Distribution Management System (DMS) - Requirements Gathering

## Introduction
This document is designed to collect the necessary business requirements for the new system. Please answer the questions in each section as thoroughly as possible. Your answers will help the technical team build a system that matches your exact needs. If a question is not applicable, simply mark it as "N/A".

---

## 1. Data Schemas (Information to Store)
For each of the categories below, please list the specific details (fields) we need to collect and store. We have provided some examples to help you get started.

### 1.1 Master User
*The core account information for anyone logging into the system.*
* **What information do we need?** *(e.g., Username, Email, Password, Status (Active/Inactive), Last Login Date)*
* **Your Requirements:** 

### 1.2 User Profile
*The detailed personal and professional information attached to a Master User.*
* **What information do we need?** *(e.g., Full Name, Phone Number, Job Title, Department, Profile Picture)*
* **Your Requirements:** 

### 1.3 Company
*The organization or business entities using the system.*
* **What information do we need?** *(e.g., Company Name, Registration Number, Tax ID, Address, Primary Contact Person)*
* **Your Requirements:** 

### 1.4 Distribution
*The logistics and movement of products.*
* **What information do we need?** *(e.g., Dispatch Date, Expected Delivery Date, Vehicle Details, Driver Name, Route/Zone, Status (Pending/In Transit/Delivered))*
* **Your Requirements:** 

### 1.5 Product
*The goods being managed and distributed.*
* **What information do we need?** *(e.g., Product Code/SKU, Name, Description, Category, Unit Price, Weight, Dimensions, Minimum Stock Level)*
* **Your Requirements:** 

### 1.6 Levels (Hierarchy)
*How the business is organized across different structures. Please define the tiers for each.*
* **Geographical Hierarchy:** How are regions broken down? *(e.g., Country -> State -> City -> Zone -> Territory)*
    * **Your Requirements:** 
* **Operational Hierarchy:** How are operations structured physically? *(e.g., Main Warehouse -> Regional Hub -> Local Distribution Center)*
    * **Your Requirements:** 
* **Structural/Organizational Hierarchy:** How are your teams structured? *(e.g., National Director -> Regional Manager -> Area Supervisor -> Field Agent)*
    * **Your Requirements:** 

### 1.7 Scheme Builder
*The rules for promotions, discounts, or special offers.*
* **What information do we need?** *(e.g., Scheme Name, Start Date, End Date, Target Audience, Eligibility Criteria, Discount Percentage/Amount, Applicable Products)*
* **Your Requirements:** 

---

## 2. Data Flow
*How information moves from one area to another. Please describe the ideal processes.*

* **Example:** When a new *Product* is added, how does it get assigned to a *Distribution* route? Who needs to be notified?
* **Example:** When a *Scheme* is created, how is it applied to a *Company* or *User*? Does it happen automatically or manually?
* **Your Requirements (Describe the key data movements and triggers):** 

---

## 3. Schema Dependencies
*Rules about what data MUST exist before something else can be created.*

* **Example:** Can a *Distribution* record be created if the *Company* hasn't been approved yet? (No)
* **Example:** Can a *User Profile* be created without first setting up a *Master User* account? (No)
* **Example:** Can a *Scheme* be applied to a *Product* that is marked as 'Out of Stock'?
* **Your Requirements (List any strict dependencies between the categories in Section 1):** 

---

## 4. Interface Flow (User Experience)
*How users will navigate through the screens to accomplish tasks.*

* **Example:** After logging in, what is the first screen an Area Supervisor sees versus a Field Agent? What data is on their dashboard?
* **Example:** What are the exact steps a manager takes to create a new Scheme? *(e.g., Step 1: Basic Info -> Step 2: Select Target Products -> Step 3: Set Discount -> Step 4: Review & Publish).*
* **Your Requirements (Describe the step-by-step journey for key tasks):** 

---

## 5. Major and Minor Checks (Validations)
*Rules the system must enforce to prevent errors and ensure data quality.*

### 5.1 Major Checks (Strict Rules - The system MUST block the action)
* **Example:** A *Product* cannot be deleted if it is currently tied to an active *Distribution* manifest.
* **Example:** A *Scheme* cannot have an end date that occurs before its start date.
* **Example:** A *Company* cannot be registered with a Tax ID that already exists in the system.
* **Your Requirements:** 

### 5.2 Minor Checks (Warnings - The system allows the action but gives a warning prompt)
* **Example:** Warn the user if they are creating a *Company* profile without providing a primary contact phone number.
* **Example:** Warn the dispatcher if a *Distribution* vehicle is assigned a load that is at 95% of its maximum capacity.
* **Your Requirements:** 

---

## 6. Major and Minor Functions (Features)
*What the system needs to actually DO within these modules.*

### 6.1 Major Functions (Core Features - The system cannot launch without these)
* **Example:** Ability to generate and print a daily distribution manifest.
* **Example:** A calculation engine that automatically applies *Scheme* discounts to eligible *Company* orders.
* **Example:** Role-based access control (e.g., Managers can edit, Users can only view).
* **Your Requirements:** 

### 6.2 Minor Functions (Nice-to-Have Features - Helpful, but can be added in later updates)
* **Example:** Ability to export the *User Profile* list to a PDF or Excel file.
* **Example:** Bulk-uploading new *Products* via a CSV spreadsheet upload.
* **Example:** Email notifications sent out when a *Scheme* is about to expire.
* **Your Requirements:** 