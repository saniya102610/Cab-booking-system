# 🚖 Cab Booking System – SQL Project

This project is a **Cab Booking System simulation** built using SQL. It demonstrates database design, data management, and analytical querying in a real-world transportation scenario.

---

## 📌 Project Overview

- Designed a relational database for cab booking operations  
- Created tables for customers, drivers, and rides  
- Inserted sample data for real-world simulation  
- Wrote SQL queries for analytics and reporting  

---

## 📂 Project Structure

| File Name      | Description |
|---------------|------------|
| schema.sql    | Creates database tables |
| data.sql      | Inserts sample data |
| queries.sql   | Contains analytical queries |
| README.md     | Project documentation |

---

## 🗄️ Database Schema

### Customers
- CustomerID (Primary Key)  
- Name  
- Phone  
- Email (Unique)  
- JoinDate  

### Drivers
- DriverID (Primary Key)  
- Name  
- Phone  
- LicenseNumber  
- Rating  
- JoinDate  

### Rides
- RideID (Primary Key)  
- CustomerID (Foreign Key)  
- DriverID (Foreign Key)  
- StartTime  
- EndTime  
- PickupLocation  
- DropLocation  
- Fare  

---

## 📊 Example Queries

### 🔹 Total Rides per Driver
```sql
SELECT DriverID, COUNT(*) AS TotalRides
FROM Rides
GROUP BY DriverID;
