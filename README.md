mysql_project
MySQL project for managing cinema show schedules and processing movie ticket bookings.
Movie Ticket Booking Project (MySQL)

Student Name: Sreepada Anirudh
Project: Individual Database Submission

About the Project
This is a MySQL database system designed to handle theater shows, schedules, and customer ticket bookings for cinema halls in Vijayawada. It uses a relational database structure split into two tables to stop data duplication and keep the fields clean.

table Structures & Relationships

1. THEATERS_AND_MOVIES (Parent Table)
Keeps track of the theater names, physical areas, movie titles, show timings, screens, and prices.
Uses SCHEDULE_ID as the main Primary Key anchor.

2. MOVIETICKET_BOOKING_ENGINE (Child Table)
Stores customer booking records, assigned seat numbers, payment types, and discount coupons.
BOOKING_STATUS automatically sets to 'BOOKED' by default for every new row.
Uses a FOREIGN KEY on SCHEDULE_ID that links directly back to Table 1 so you cannot book a ticket for a fake show number.

Key SQL Operations Implemented
Table Creation & Foreign Key Configuration: Built both relational table structures cleanly with matching data types.
Real Data Ingestion: Inserted data records for active local shows (Ravindra Cinemas, Tara Screens, G3 Rajyuvraj) and mock customer bookings.
Live Data Updates: Coded queries to update ticket costs based on high demand and to change booking statuses for seat cancellations.
Analytical Reporting: Used an INNER JOIN to cross-reference both tables and print a single-customer billing receipt filtered by name.

System Details
Database Tool: MySQL Server 8.0 & MySQL Workbench
Language: SQL
