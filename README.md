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
