
<img width="1364" height="1104" alt="Parking_DB_Design" src="https://github.com/user-attachments/assets/241e19ec-5564-490b-8fc7-406467acaf69" />

# Smart Venue Parking Management System – Database Design

This project presents the database design for a smart venue parking management system used in large-scale events such as expos, concerts, trade fairs, and sports tournaments. The system is designed to efficiently manage thousands of vehicles across multiple parking areas while ensuring smooth entry, allocation, monitoring, and payment handling.

---

## Overview

The system is responsible for managing:

* Vehicle registration and parking activity
* Smart parking slot assignment
* Multi-level and multi-zone parking operations
* Reserved parking allocations for premium users and staff
* Digital ticket generation and validation
* Parking fee calculation based on duration and category
* Live parking availability monitoring
* Entry and exit management using automated tracking

---

## Main Entities

### Vehicles

Stores information related to vehicles entering the venue.

Attributes may include:

* Vehicle ID
* License Number
* Vehicle Type
* Owner Details
* Electric Vehicle Support

### Vehicle Types

Defines different categories of vehicles.

Examples:

* Car
* Bike
* SUV
* Bus
* Electric Vehicle

### Parking Areas

Represents parking sections available inside the venue.

Attributes may include:

* Area ID
* Zone Name
* Floor Number
* Capacity

### Parking Slots

Stores information about individual parking spaces.

Attributes may include:

* Slot ID
* Availability Status
* Slot Type
* Assigned Area

### Slot Categories

Defines compatibility rules between slots and vehicles.

Examples:

* Compact Vehicle Slot
* Heavy Vehicle Slot
* EV Charging Slot
* Accessible Parking Slot

### Reserved Access Categories

Handles reserved parking allocations.

Examples:

* VIP Parking
* Staff Parking
* Organizer Parking
* Emergency Vehicle Parking

### Parking Records

Acts as the central entity that tracks parking activity.

Stores:

* Entry Time
* Exit Time
* Allocated Slot
* Vehicle Information
* Parking Duration

### Parking Passes

Generated whenever a parking session starts.

Includes:

* Pass Number
* Entry Timestamp
* QR Code or Barcode Details
* Session Reference

### Transactions

Stores payment and billing details.

Includes:

* Payment ID
* Payment Method
* Total Amount
* Payment Status
* Transaction Time

---

## System Relationships

* One vehicle can create multiple parking records over time.
* One parking slot can be assigned to different vehicles during separate sessions.
* Parking records connect vehicles, slots, passes, and transactions.
* Parking availability is updated dynamically using active parking records.
* Reserved access categories control slot allocation priority.
* Vehicle types and slot categories ensure proper parking compatibility.

---

## Key Functionalities

### Parking Allocation

The system automatically assigns suitable parking slots based on:

* Vehicle type
* Slot availability
* Reserved category permissions
* Parking zone preferences

### Entry and Exit Tracking

Tracks real-time movement of vehicles entering and leaving the venue.

### Real-Time Availability

Displays available parking spaces instantly to administrators and users.

### Billing and Payments

Calculates parking charges according to:

* Parking duration
* Vehicle category
* Reserved access privileges

### Security and Monitoring

Supports monitoring features such as:

* Vehicle verification
* Unauthorized parking detection
* Digital parking logs

---

## Design Objectives

The purpose of this database design is to create a scalable and efficient parking management system by separating:

### Infrastructure Layer

Includes:

* Parking areas
* Parking slots
* Slot categories

### Operational Layer

Includes:

* Parking records
* Parking passes
* Vehicle movement tracking

### Access Control Layer

Includes:

* Reserved parking categories
* Vehicle-slot compatibility rules

### Financial Layer

Includes:

* Transactions
* Billing
* Payment processing

---

## Expected Benefits

* Faster vehicle management during large events
* Reduced congestion and manual effort
* Better parking space utilization
* Accurate billing and transaction tracking
* Improved security and operational monitoring
* Easy scalability for large venues and future expansion

---

## Conclusion

This database design demonstrates how a smart venue parking management system can efficiently organize vehicle operations from entry to exit. By combining parking allocation, tracking, billing, and reservation management into a structured relational model, the system supports reliable and scalable parking operations for high-traffic events and venues.

