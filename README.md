# 🚗 Event Parking Management System – ER Diagram

This project models the database design for a multi-zone event parking system (e.g., Comic-Con India), where thousands of vehicles are managed across zones, levels, and reserved categories.
<img width="1364" height="1104" alt="Parking_DB_Design" src="https://github.com/user-attachments/assets/241e19ec-5564-490b-8fc7-406467acaf69" />


## 📌 Overview

The system handles:
- Vehicle entry and exit tracking
- Parking spot allocation across zones and levels
- Reserved parking (VIP, staff, exhibitors, EV charging, etc.)
- Ticket generation for each parking session
- Payment processing based on parking duration
- Real-time parking availability

## 🧱 Core Entities

- **Vehicles** – Stores vehicle details (type, license plate, EV support)
- **Vehicle Categories** – Defines vehicle types (car, bike, SUV, etc.)
- **Parking Zones** – Represents different zones/levels in the venue
- **Parking Spots** – Individual spots within zones
- **Spot Types** – Defines compatibility of spots with vehicle types
- **Reserved Categories** – Special allocations (VIP, staff, EV, etc.)
- **Parking Sessions** – Tracks entry, exit, and spot usage
- **Parking Tickets** – Issued per parking session
- **Payment Records** – Stores payment details for each session

## 🔗 Key Concepts

- A **vehicle can have multiple parking sessions** across days  
- A **parking spot can be reused** across different sessions  
- **Parking sessions are the core entity**, linking vehicle, spot, ticket, and payment  
- **Spot availability is derived** from active sessions (no exit time)  
- **Reserved categories and spot types** control allocation logic  

## 🎯 Goal

The goal of this design is to model a scalable and realistic parking system by separating:
- **Infrastructure** (zones, spots, types)
- **Operations** (sessions, tickets)
- **Business rules** (reservations, compatibility)
- **Financials** (payments)

---

📊 The ER diagram illustrates how vehicles move through the parking system from entry to exit, including spot assignment and payment processing.
