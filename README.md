# PYTHON ASSIGNMENT
Name: Thapelo Titus Malao
StudentID: bida25-482
Module: Introduction to Python
Assignment component: Section A-C

Section A:Data entry and validation
The user is required to insert the number of students and it should be greater than 0. The program will reiterate the student names and grades the amount of times that equate to each student. The input for the student names and cannot be null.
Each grade is validated and must be a number that lies between 0 and 100. Invalid entries are rejected with a message and the question is repeated.

Calculations and Reporting:
After all data is entered, the program displays:
• Class total and class average: Calculates and displays these metrics across all grades collected.
• Student vs. class average comparison: Shows the average grade per student directly next to the overall class average.
• Highest and lowest grade per subject: Identifies the top and bottom performing scores for each individual subject.
• Formatted summary table: Displays every student's grades alongside their final average in a clean, readable layout.

Section A+B Data Structure:
Section A+B starts with the students and subjects variables assigned to lists in order to cater for mutability and editing during insertion of values. As the code progress the list is appended to a multi datatype tuple to avoid changing of data values once the values are stored.

Section C:
The program is an interactive system, the program loops on a main menu until the user chooses Exit.
The menu option has the following;
• Add a new Student: It asks for a name and all subject grades.
• Update an existing student's grades: Updates all grades for a student who already exists.
• Remove a student: It deletes the student by name.
• Search for a Student: It shows the student's grades per subject and their average.
• View subject specific grades: Chooses a subject by number and list every student's grade for it.
• View full class summary and report: Displays totals, averages, highest/lowest, and a summary table for the data about students that was inserted.
• Exit: It ends the program.

Section C data structure:
The data structure for section C is a dictionary and the student names are keys whereas the grades are values. The use of a dictionary helps give fast lookups by name for search, update and remove, and keeps grades labelled by subject.
