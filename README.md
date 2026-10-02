# Learning python :)
I'm Vanya of school of Engineering in Monash University learning coding from the Faculty of Information and Technology: FIT1056. 
Check out my branch: vanyac10-fit1056-pst. 

print("see you there!")


Music School Management System (MSMS) - GUI Edition
Project Overview
This project represents Stage 4 (PST4) of the MSMS development journey. The goal of this iteration is to replace the previous text-based console with a modern Graphical User Interface (GUI) built using Streamlit. The application allows receptionists to manage student registrations, view daily class rosters, and perform student check-ins seamlessly.   
PDF
+ 2

Application Structure (What Each Part Does)
The project strictly separates the business logic from the user interface:   
PDF

main.py: The entry point of the application, responsible solely for launching the GUI.   
PY
+ 1

gui/main_dashboard.py: Acts as the central hub. It configures the Streamlit page layout, initializes the backend ScheduleManager in the session state to ensure data persists during navigation, and renders the sidebar menu.   
PDF

gui/student_pages.py: Contains the UI components for the "Student Management" module, handling the search logic and the "Register Student" form.   
PDF

gui/roster_pages.py: Contains the UI components for the "Daily Roster" module. It displays today's classes using a Pandas DataFrame and houses the interactive check-in form.   
PDF

app/ Directory: Contains the core Object-Oriented business logic (schedule.py, student.py, teacher.py, user.py) perfected in PST3, which handles object creation and JSON data serialization.   
PDF
+ 4

How to Run and Test
Prerequisites
Ensure you have Python installed, then install the required external libraries via your terminal:   
PDF

Bash
pip install streamlit pandas
Running the Application
Navigate to the root directory of the project in your terminal and execute the following command:   
PDF
+ 1

Bash
streamlit run main.py
Testing the Full Program
Navigation: Use the sidebar to switch between the Home, Student Management, and Daily Roster pages.

Registration: Go to "Student Management", register a new student with a name and instrument, and verify the success message.   
PDF

Search: Test the search function using the newly created Student ID.   
PDF

Check-In: Go to "Daily Roster", view the active classes in the table, and use the dynamic dropdowns to check a student into a valid course.   
PDF

Data Persistence: Stop the server (Ctrl+C in the terminal), restart it, and verify that your new students and check-in records were successfully saved to data/msms.json.   
PY

Design Choices and Assumptions
Separation of Concerns: I kept all st. GUI elements strictly inside the gui/ directory, while data manipulation remains inside app/schedule.py. This ensures the backend can be reused independently of the interface.   
PDF

Session State Management: Because Streamlit reruns the script upon every interaction, I instantiated ScheduleManager inside st.session_state. This prevents the application from inefficiently reloading the JSON file from scratch on every button click.   
PDF

Dynamic Roster Dropdowns: For the check-in form, I used dynamic dropdown menus containing both the names and IDs. This prevents backend ID assignment errors in cases where two students share the same first name.

Assumptions: I assumed the data/msms.json file is correctly formatted. If the file is entirely missing, the backend is configured to catch the FileNotFoundError and gracefully start with empty lists.   
PY

Once you have saved this file, run your final set of Git commands to add it to your submission:
git add README.md
git commit -m "docs: Add comprehensive README explaining architecture, setup, and design choices"
git push origin individual
