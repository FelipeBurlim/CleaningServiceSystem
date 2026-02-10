# Cleaning Service Management System 
A Python-based application designed for cleaning service providers to manage staff (cleaners), clients, and service contracts with full data persistence.

## Project Overview
This project manages the operational workflow of a cleaning business, ensuring that all data is stored securely in text files and that business logic prevents duplicate entries for primary keys.

### Core Entities
The system is built around three main data structures:
* **Cleaners (Key: CPF):** RG, Name, Gender, Birth Date, Phone Numbers.
* **Clients (Key: CPF):** Name, Birth Date, Address, ZIP Code (CEP), City, Emails, Phone Numbers.
* **Services (Composite Key: CPF Cleaner + CPF Client + Date):** Service Date, Total Value.

## System Navigation
The interface is driven by a main menu that leads to specific management submenus:

### Menu Structure
1. **Cleaners Submenu:** Manage cleaning staff records.
2. **Clients Submenu:** Manage customer contact and location data.
3. **Services Submenu:** Register and track cleaning appointments.
4. **Reports Submenu:** Access business intelligence and history.
5. **Exit:** Terminate the program and save all data.

### Standard Operations
Within each submenu (Cleaners, Clients, Services), the following operations are available:
* **List All:** View every record in the database.
* **List One:** Search for a specific entry using its Primary Key.
* **Include:** Add new data (validation prevents duplicate CPFs).
* **Update:** Edit existing information.
* **Delete:** Remove a record after an explicit confirmation prompt.

## Reporting System
The system generates specialized reports that are automatically saved to text files:
* **Customer Contact List:** Displays names, emails, and phones of all clients who hired a specific cleaner within a given date range (Date X to Date Y).
* **Daily Schedule:** Lists all services scheduled for a specific date, including the names of both the cleaner and the client.
* **Cleaner History:** Provides a full history of all services performed by a specific cleaner based on their CPF.

## Technical Requirements
### Data Architecture
* **Persistence:** Data is stored in `faxineiros.txt`, `clientes.txt`, and `servicos.txt`. Reports are also exported to text files.
* **Modular Logic:** The program uses functions for every operation. No global variables are used; data flows through the system strictly via parameters and return values.
* **Conflict Prevention:** The system enforces unique constraints on CPFs to ensure data integrity.

## Installation and Usage
1. **Requirements:** Python 3.x.
2. **Setup:**
   ```bash
   git clone [https://github.com/FelipeBurlim/CleaningServiceSystem.git](https://github.com/FelipeBurlim/CleaningServiceSystem.git)
   cd CleaningServiceSystem
