# 🚌 Bus Reservation System with JDBC

This is a simple **console-based Bus Reservation System** written in **Java**.  
It allows passengers to book tickets, checks seat availability, and stores booking details in a **MySQL database** using **JDBC**.

---

## ✨ Features
- View all available buses with details (bus number, AC/Non-AC, capacity).
- Book tickets by entering passenger name, bus number, and travel date.
- Prevents overbooking by checking seat availability against capacity.
- Stores bus details and passenger bookings in **MySQL** database.
- Demonstrates **OOP principles** and **JDBC database connectivity**.

---

## 🛠️ Technologies Used
- **Java (JDK 8+)**
- **JDBC**
- **MySQL Database**
- **Eclipse / IntelliJ IDEA** (any Java IDE works)

---

## 📂 Database Setup
1. Install MySQL (or use XAMPP/MAMP).
2. Create a database:
```
CREATE DATABASE bus_reservation;
USE bus_reservation;
```
3.Create tables:
```
CREATE TABLE buses (
    bus_no INT PRIMARY KEY,
    ac BOOLEAN,
    capacity INT
);

CREATE TABLE bookings (
    id INT AUTO_INCREMENT PRIMARY KEY,
    passenger_name VARCHAR(50),
    bus_no INT,
    booking_date DATE,
    FOREIGN KEY (bus_no) REFERENCES buses(bus_no)
);
```
4.Insert sample bus data:

```
INSERT INTO buses VALUES
(1, TRUE, 3),
(2, FALSE, 3),
(3, TRUE, 3);
```

## 📸 Sample Output

---
Bus No :1   AC:true   Total Capacity:3
Bus No :2   AC:false  Total Capacity:3
Bus No :3   AC:true   Total Capacity:3
Enter 1 to book or 2 to exit
1
Enter name of passenger:
John
Enter bus no:
1
Enter date DD-MM-YYYY
25-08-2025
Your booking is confirmed
---

## 🎯 Learning Outcomes

---
Java OOP (Classes, Objects, Encapsulation, Methods)

Exception Handling

User Input Handling (Scanner)

JDBC Database Connectivity

SQL (DDL & DML commands)
---
