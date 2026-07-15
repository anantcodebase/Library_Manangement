# Library Management System

A lightweight, console-based Library Management System implemented in C++. This application demonstrates core Object-Oriented Programming (OOP) concepts by decoupling user behaviors from centralized library records. It provides an interactive interface for managing book inventories, tracking member activities, and processing book loans.

## Key Features

* **Book Inventory Management:** Allows administrators to view the complete catalog of available books alongside their respective prices and dynamically append new titles to the collection.
* **Borrowing System:** Enables members to search for and borrow specific titles from the library. The system automatically fetches real-time pricing data and prevents duplicate checkouts of the same book by a single user.
* **Integrated Return Pipeline:** A dedicated feature that allows users to return books, instantly updating their profile by removing the title and adjusting their active balance/borrowed history.
* **Member Account Profiles:** Displays individual profile dashboards containing personal identity information and an itemized overview of currently checked-out assets.

## Architecture & Data Flow

The project is structured around two primary classes to ensure a modular separation of concerns:

1. **`Library` Class:** Acts as the central database, managing global data collections for book titles (`collection`) and pricing indices (`price`).
2. **`User` Class:** Manages runtime instances of individual members, storing localized states such as personal identifiers and isolated transactional vectors (`borrowed` and `borrowedprice`).

## Technologies Used

* **Language:** C++ (C++11 or higher recommended)
* **Standard Template Library (STL):** Heavily utilizes `std::vector` for dynamic memory allocation and collection tracking, alongside `std::string` for robust text processing.
