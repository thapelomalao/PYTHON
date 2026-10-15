SECTION D README
PYTHON VERSION used: 3.13 version
Student Management System

A python program for managing student grades. Students can be added, updated, removed, searched, and compared through a simple numbered menu. This program is organised using functions with input validation and error handling techniques.

The program is an interactive system, the program loops on a main menu until the user chooses Exit.

The menu option has the following:

Add a new Student: It asks for a name and all subject grades.
Update an existing student's grades: Updates all grades for a student who already exists.
Remove a student: It deletes the student by name.
Search for a Student: It shows the student's grades per subject and their average.
View subject specific grades: Chooses a subject by number and list every student's grade for it.
View full class summary and report: Displays totals, averages, highest/lowest, and a summary table for the data about students that was inserted.
Exit: It ends the program.
Section C Data Structure
The data structure for section C is a dictionary and the student names are keys whereas the grades are values.

The use of a dictionary helps give fast lookups by name for search, update and remove, and keeps grades labelled by subject.

ERROR HANDLING:
To avoid errors whereby the user did not insert the right data type or value expected, the code is written using the try and exceptValue error, to make sure that the 
user inserts the right input. An example of where this is enforced is in the get_valid_grade function.
