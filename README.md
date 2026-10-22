# Python coding!!
Hi! I'm an undergraduate engineering student at Monash University learning how to code Python. These codes in my "vanyac10-fit1056-pst" are for a Music School Management System Prototype/Code. This was done for a school practical project that allows us students to code and add new ideas into the code. I have explored coding functions which are interesting and wanted to share it with you. 

# Music School Management System (MSMS) 

A lightweight, persistent command-line application built in Python for managing a music school's daily operations. This system handles student and teacher records, tracks attendance, and generates student ID badges, saving all data locally via a JSON database.

## Features

* **Data Persistence:** Automatically saves and loads data using a local `msms.json` file. You never lose your records when the application closes.
* **Student & Teacher Management:** Full CRUD (Create, Read, Update, Delete) capabilities to easily update contact information, instruments, and specialities.
* **Receptionist Tools:**
  * **Student Check-in:** Records student attendance for specific courses with automated datetime stamping.
  * **ID Badge Generation:** Prints formatted student ID cards into standalone text files (e.g., `1_card.txt`).
* **Error Handling:** Includes `try-except` blocks to prevent crashes when invalid data (like text instead of ID numbers) is entered.

## Prerequisites

This project requires **Python 3.x** to run. It uses only built-in Python libraries (`json` and `datetime`), so no external packages or `pip install` commands are required.

## How to Run

1. Clone this repository to your local machine:
   ```bash
   git clone [https://github.com/yourusername/msms-python.git](https://github.com/yourusername/msms-python.git)


   # Music School Management System (MSMS) - GUI Edition

## Project Overview
This project represents Stage 4 (PST4) of the MSMS development journey. The goal of this iteration is to replace the previous text-based console with a modern Graphical User Interface (GUI) built using Streamlit. The application allows receptionists to manage student registrations, view daily class rosters, and perform student check-ins seamlessly.

## Application Structure (What Each Part Does)
The project strictly separates the business logic from the user interface:
* **`main.py`**: The entry point of the application, responsible solely for launching the GUI.
* **`gui/main_dashboard.py`**: Acts as the central hub. It configures the Streamlit page layout, initializes the backend `ScheduleManager` in the session state to ensure data persists during navigation, and renders the sidebar menu.
* **`gui/student_pages.py`**: Contains the UI components for the "Student Management" module, handling the search logic and the "Register Student" form.
* **`gui/roster_pages.py`**: Contains the UI components for the "Daily Roster" module. It displays today's classes using a Pandas DataFrame and houses the interactive check-in form.
* **`app/` Directory**: Contains the core Object-Oriented business logic (`schedule.py`, `student.py`, `teacher.py`, `user.py`) perfected in PST3, which handles object creation and JSON data serialization.

## How to Run and Test
### Prerequisites
Ensure you have Python installed, then install the required external libraries via your terminal:
```bash
pip install streamlit pandas
```
# PST5 - Management System

A robust, object-oriented Python application featuring a Streamlit web GUI, JSON-based data persistence, and a comprehensive `pytest` testing suite. This system is designed to handle complex organizational workflows including role-based user management, inventory tracking, financial/donation logging, and task delegation.

## Key Features

*   **Role-Based User Architecture:** Distinct user models (`AdminUser`, `StaffUser`, `DonorUser`, `VolunteerUser`, `ClientUser`) with customized access scopes and data relationships.
*   **Security & Authentication:** Integration of `bcrypt` for secure password hashing, automatic legacy password upgrading, and strict name/password complexity validation.
*   **Data Persistence & Backup:** Reliable JSON file storage with automated, timestamped backups to prevent data loss.
*   **Inventory & Logistics Management:** 
    *   Dynamic inventory tracking with minimum stock thresholds and auto-recorded transaction audit logs.
    *   Supply assembly workflows (packing/unpacking hampers, collecting/stocking donations) with automatic stock deduction and restoration.
*   **Task & Issue Tracking:** Assignment of tasks to volunteers, ability to take over jobs, and a complete issue-flagging and resolution system.
*   **Client Messaging:** Built-in messaging system for clients to send, edit (with timestamp tracking), and delete messages.
*   **Streamlit Web Dashboard:** Interactive sidebar navigation, data metric summaries, and modular GUI pages.
*   **Extensive Unit Testing:** Over 60 isolated tests using `pytest` ensuring 100% coverage of core business logic, exception handling, and cascade deletions.

## Technologies Used

*   **Python 3** (Core backend logic and object-oriented models)
*   **Streamlit** (Frontend GUI dashboard)
*   **Pytest** (Automated unit testing suite)
*   **Bcrypt** (Cryptographic password hashing)
*   **JSON** (Local database storage)

## Project Structure

```text
├── app/
│   ├── FoodBank.py         # Main controller and business logic
│   ├── inventory.py        # Stock and transaction management
│   ├── utils.py            # Logging, backups, and data validation
│   ├── admin.py, client.py # User role classes
│   └── ...
├── gui/
│   ├── main_dashboard.py   # Streamlit app configuration and routing
│   ├── home_page.py        # Landing page with system metrics
│   └── ...
├── tests/
│   └── test_food_bank.py   # Comprehensive pytest suite
├── data/
│   └── data.json           # Main JSON database (auto-generated)
└── main.py                 # Application entry point
