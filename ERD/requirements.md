# ER Diagram — alx-airbnb-database

## Files
- ERD/airbnb_erd.png

## Description
This ER diagram models an Airbnb-style database system for managing users, properties, bookings, payments, reviews, and messages.  
It captures the key entities, their attributes, and relationships, ensuring data integrity through foreign keys, constraints, and indexes.

---

## Entities and Attributes

### User
- user_id (PK, UUID, Indexed)
- first_name (VARCHAR, NOT NULL)
- last_name (VARCHAR, NOT NULL)
- email (VARCHAR, UNIQUE, NOT NULL)
- password_hash (VARCHAR, NOT NULL)
- phone_number (VARCHAR, NULL)
- role (ENUM: guest, host, admin)
- created_at (TIMESTAMP, DEFAULT CURRENT_TIMESTAMP)

### Property
- property_id (PK, UUID, Indexed)
- host_id (FK → User.user_id)
- name (VARCHAR, NOT NULL)
- description (TEXT, NOT NULL)
- location (VARC
